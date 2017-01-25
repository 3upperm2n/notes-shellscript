### extract code block number from the isa file
CodeXL can extract the isa from your runtime kernel. Each code block in the isa begins with the label_xxxx. 
```bash
label_0021:
  s_andn2_b64   exec, s[0:1], exec                          // 00000084: 8AFE7E00
  s_cbranch_execz  label_0755                               // 00000088: BF880732
```

The following command can find the number of code blocks.
```bash
sed -n '/^label_/p' b0_macro.isa  | wc -l
```
