# First step - find 'touch3' function's address

Let's start with open 'ctarget' program through gdb.

1. `gdb > disas touch3`

	touch3's address : 0x4018fa

# Second step - analysis 'touch3' and 'hexmatch'

What's function hexmatch's work?

- It matches cookie and input string, "return (match) 0x01 : 0x00"

Let's find two memory addresses (or register)  matched by hexmatch.

```assembly
<script>
	
</script>

```

We can know hexmatch function matches *%rdi and cookie value in stack address 0x5561dc13.

---
In order to pass hexmatch, the value pointed by %rdi and the value in address 0x5561dc13 must be the same.

Then one solution might be set the %rdi to the stack address 0x5561dc13. Then apparently both value is the same.


# Third step - Wrtie assembly code to 
