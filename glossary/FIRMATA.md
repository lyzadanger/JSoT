[**Firmata**](https://github.com/firmata/protocol) is a defined _protocol_ for communicating between a host computer's software and a microcontroller. It is based on the MIDI messaging format. It makes it possible to write logic for microcontrollers using higher-level languages.

Its most complete and well-known _implementation_ of firmata is for Arduino-compatible boards ([firmata/arduino](https://github.com/firmata/arduino)).

The Arduino _implementation_ of _firmata_ in turn has numerous _libraries_ for different programming languages. Libraries are available for Java, JavaScript, PHP, ruby, python, etc.

Finally, some frameworks implement _adapters_ to language-specific _libraries_.

[`cylon-firmata`](https://github.com/hybridgroup/cylon-firmata) is an _adapter_ between the [`cylon.js`](http://cylonjs.com/) framework and the _[Firmata.js](https://github.com/jgautier/firmata)_ JavaScript _library_ for the [Arduino _implementation_](https://github.com/firmata/arduino) of the [firmata _protocol_](https://github.com/firmata/protocol). Whew!

The popular [`johnny-five`](https://github.com/rwaldron/johnny-five) Node.js framework is also built on top of `firmata.js`.
