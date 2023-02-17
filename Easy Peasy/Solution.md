## Screenshot

### This screenshot shows first half of the screen solution
![alt text](https://github.com/Gul31/PicoCTF/blob/main/Easy%20Peasy/Sol%201.PNG?raw=true)

### This screenshot shows second half of the screen solutio
![alt text](https://github.com/Gul31/PicoCTF/blob/main/Easy%20Peasy/Sol%202.PNG)

## Command used

- `wget` (link of the otp file given in CTF)
- `python -c "print('a'*49968);print('a'*32)" | nc mercury.picoctf.net 41934`
- `nc mercury.picoctf.net 41934`      \\ given in the question

- `python`   \\ to run python module
- `ef=0x0346303d1902033d1959003d1903553d1951553d1907593d1951511a3d190505`    #assign three variables ef,ea,pa to perform a XOR operation
- `ea=0x0345376e1e5406691d5c076c4050046e4000036a1a005c6b1904531d3941055d`
- `pa=0x6161616161616161616161616161616161616161616161616161616161616161`
- '{:x}'.format(ef^ea^pa)

Solution will be hex string: **6162663266376435656466303832303238303736626664376134636665396139**
