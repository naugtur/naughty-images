# naughty images

## SVG Images with XSS in them.

A collection of SVG XSS samples I created, found or recreated. 
Some of them may not work. 

- 0x are pure xss
- 1x require user interaction
- 2x are DOS
- 3x are other shenanigans

## CVE-2023-4863 PoC copy

https://blog.isosceles.com/the-webp-0day/

`webp/` contains a copy of the PoC webp out-of-bound write.  
Unfortunately it doesn't have an exploit in it so it's hard to tell if you're getting an error from a vulnerable webp version or an error from patched webp that throws for an incorrect Huffman codes table.

```
gcc -o craft craft.c
./craft bad1.webp
```