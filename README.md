# shellscript-note
##### loop
```bash
for (( N=2; N<1048576; N++))
do
# step 1: profile
  nvprof --print-gpu-summary --csv ./h2d 1 0 $N > tmp.csv 2>&1

  for (( i=1; i<10; i++ ))
  do
    nvprof --print-gpu-summary --csv ./h2d 1 0 $N >> tmp.csv 2>&1
  done

## step 2： append the results 
  ./parse_nvprof_summary.py $N >> 1stream_1_1M.log
done
```
