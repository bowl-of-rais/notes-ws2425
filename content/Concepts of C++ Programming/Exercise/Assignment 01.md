- [x] TODO get clion to understand the targets 📅 2024-10-23 ✅ 2024-10-21
- [ ] TODO understand tasks + make tasks lists 📅 2024-10-23 
- [ ] TODO complete assignment 📅 2024-10-27


# Mandelbrot

```cpp
void mandelbrot(double realCenter, double imagCenter, double width, double height) {
	// TODO
}
```

goal:
- compute + print image of mandelbrot set
- rectangular image: 
	- 200 characters wide
	- same aspect ratio as given by `{cpp} width` and `{cpp} height`
		- note: font has aspect ratio **0.4**

program logic:
- calculate output pixels
- iterate over output pixels
	- compute complex number by linear interpolation
	- iteratively compute $z(i+1) = f_{c}(z_i)$ with $z_{0}= 0$
		- $f_{c}(z_{i}) = z^{2} + c$
		- if $abs(z_{i}) > 2$: assume divergence ->  print ` `
		- if no divergence for 200 iterations: assume $c$ is in set -> print `x`
## Tasks

- [x] TODO make code structure 🆔 k49bq2 📅 2024-10-23 ✅ 2024-10-22
- [x] TODO implement aspect ratio calculation 🆔 i7kcbo ⛔ k49bq2 📅 2024-10-27 ✅ 2024-10-22
- [x] TODO implement interpolation ⛔ k49bq2 📅 2024-10-27 ✅ 2024-10-22
- [x] TODO implement iterative computation of $f_{c}$ ⛔ k49bq2 📅 2024-10-27 ✅ 2024-10-22
- [x] TODO check tests/fix bugs ✅ 2024-10-22


# Simple VM

```cpp
int32_t execute() {
	return 0;
}
```

goal: 
- VM with 4 integer (32bit) and 2 floating point registers + arithmetic operations
- instructions as input stream -> `{cpp} next()`
	- opcode: `{cpp} int32_t` between 0 and 100
	- 0 or more arguments: `{cpp} int32_t` either a register identifier (0..3) or integer immediate
- **wrap on over- and underflow!**
- special case: division by zero

program logic:
- loop until halt instruction:
	- get next opcode from stream
	- depending on opcode, get arguments from stream
	- switch based on opcode: execute instruction