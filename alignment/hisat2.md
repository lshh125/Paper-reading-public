https://github.com/jmzeng1314/scRNA_smart_seq2/blob/master/shell.txt

Build index
```bash
hisat2-build -p 16 genome.fa genome
```


Align and count
```bash
index=smartseq2-ref/grch38/genome
module add hisat2/2.1.0
ls fastq/*_R1_*gz | while read id; do 
hisat2 -p 10 -x $index -1 $id -2 ${id/_R1_/_R2_} -S ${id%%_R1_*}.hisat.sam
done 
mkdir sam
mv fastq/*.sam sam/


cd sam
module add samtools/1.4
ls *.sam|while read id ;do (samtools sort -O bam -@ 5  -o $(basename ${id} ".sam").bam   ${id});done
ls *.bam |xargs -i samtools index {}
mkdir ../bam
mv *.bam ../bam/
mv *.bai ../bam/


cd ../bam
module add subread/1.6.3
gtf=/rsrch3/scratch/bcb/sliang3/smartseq2-ref/gencode.v38.annotation.gtf.gz
featureCounts -T 5 -p -t exon -g gene_id  -a $gtf -o  all.id.txt  *.bam  1>counts.id.log 2>&1 &
```
