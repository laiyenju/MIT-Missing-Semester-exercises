**Q2. Create a new directory called `missing` under `/tmp`.**

1. make sure we are in the home directoy: `cd ~`
2. in home directory and input `cd /tmp`

**Q3. Look up the `touch` program. The `man` program is your friend.**

`man ls` to check the command list

**Q4. Use `touch` to create a new file called `semester` in `missing`.**

`touch semester ~/missing`

**Q5. Write the following into that file, one line at a time:**

```
#!/bin/sh
curl --head --silent https://missing.csail.mit.edu
```

one-line solution: `echo `#!/bin/sh` > semester`

**Q6. **
