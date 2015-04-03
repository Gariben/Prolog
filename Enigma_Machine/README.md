# Enigma Machine

![alt text](http://i.imgur.com/hjOIrnt.png "Sample IO on Ubuntu 12.04")

## About the Enigma Machine

The Enigma Machine is a device famously used in WWII by German forces to encrpyt messages. It worked by 
sending current through a series of "scrambled" rotors, and bouncing it from a reflection plate, in order
to produce an output that could be mirrored and, in turn, decrypted.  

[Here](http://en.wikipedia.org/wiki/Enigma_machine) is more about the history of the machine.

[Here](http://users.telenet.be/d.rijmenants/en/enigmatech.htm) are some of the more technical details of how the machine works.

## Project Scope:

This particular script is based on the *M3 model*, which features rotors *I*, *II*, *III* and a *B Reflector*.
I encourage to fork my code and make it open to other models, or for that fact, any model.
This project was compiled in GNU prolog.

## Usage:

The predicate that deploys the enigma machine is *enigma*, which has five arguments.

`enigma([Input],[A,B,C],[[X,Y],[M,N]], Output).`

The first argument is the *input string*, in the form a list.

The second argument are the *three rings* for encryption. They are in the order they are encountered, 
which is Rotor III, Rotor II and then Rotor I.

The third argument is a list of pairs that form the *plugboard*.

the fourth argument is the *output*, which should always be a variable.

### Examples:

```
| ?- enigma([b,u,t,t,e,r,f,l,y],[t,h,q],[[a,c],[b,f]],O).

O = [o,n,f,k,o,c,v,c,q]

(4 ms) yes
| ?- enigma([o,n,f,k,o,c,v,c,q],[t,h,q],[[a,c],[b,f]],O).

O = [b,u,t,t,e,r,f,l,y]

(8 ms) yes
| ?- 
```

### Credit

Thanks to the folks at [enigmaco.de](http://enigmaco.de/enigma/enigma.html) for their great visualization, which made this project go much smoother.
