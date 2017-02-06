## cnee in ubuntu
```bash
sudo apt-get install cnee
```

Record only mouse movement, and set Q as the key for exiting recording.
```bash
cnee --record --mouse -o submit.xnl -sk q
```

The previous command only replay the movement once.
Run an infinite loop to keep replaying the recorded precedure.
```bash
#!/bin/bash
while true
do
  cnee --replay -f submit.xnl -ns
  # wait for 5 mins 20 seconds
  sleep(320)
done
```

## Reference
* https://www.youtube.com/watch?v=fupThBxwp_E&t=313s
* http://manpages.ubuntu.com/manpages/precise/man1/cnee.1.html#contenttoc0
* https://xnee.files.wordpress.com/2012/10/xnee1.pdf
