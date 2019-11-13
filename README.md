Program for converting text data to binary data that makes text visible as letters on punched tape.
Punched paper tapes were popular way to store computer data in 60's - 80's. Punched tape is 1" wide paper tape that has nine data "tracks" that's used for data storage and synchronisation. Data itself are represented as small punched holes in this tape. This program can be useful if You have functional paper tape punch and You want to make some kind of retro-computing themed texts out of tape. See pictures for examples.
Program is written on Python and is tested as fully working on Raspberry Pi. In my case, prepared data is output to serial port where's connected noname tape punch from weaving machine.

Usage is simple - You run program with text as argument. You'll get binary data as output. You can forward that data to file to save or directly to serial port where tape punch is connected and text will be seen on tape. If command is run with no file or port to be forwarded, it will simply print some gibberish on screen.
Escaped hex data can be output to form unusual patterns or symbols. Escaped data is not converted in any way, it's only output as is - one byte. For example \x1E will output one byte 00011110 instead of four visible symbols.

Example commands:
- Convert text to binary and save to file:
> ./tapetext.py "some text here" > binary_text.bin

- Convert text and output binary data directly to preconfigured port:
> ./tapetext.py "some other text here" > /dev/ttyS0

- Print text "Lana" followed by heart that's made out of escaped bytes:
> ./tapetext.py "Lana\x0E\x11\x21\x41\x42\x21\x11\x0E" > /dev/ttyS0

I think ... that's it.
Oh, and if You're using this program in its intended function, feel free to contact me with your retro gear photos and results made with this program.
