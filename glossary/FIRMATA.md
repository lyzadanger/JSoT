[**Firmata**](https://github.com/firmata/protocol) is a _protocol_ based on the MIDI messaging format. Firmata enables communication between software on a host computer and the microcontroller embedded in a hardware project, making it possible to write software logic for microcontrollers using diverse, higher-level languages.

The use of firmata involves a host-client model of hardware development: a host computer runs software and communicates instructions to the microcontroller (or other processor), which behaves as a client. To accomplish this, both the software on the host computer and the firmware on the hardware need to "speak" (i.e. implement) firmata.

## Firmata Implementations

Firmata itself is a protocol and is _implemented_ for different platforms. The most popular implementation of firmata is for Arduino-compatible boards ([firmata/arduino](https://github.com/firmata/arduino)).

## Libraries for Firmata Implementations

The Arduino _implementation_ of _firmata_ in turn has numerous _libraries_ for different programming languages. Libraries are available for Java, JavaScript, PHP, ruby, python, etc.

_Example_: [firmata.js](https://github.com/jgautier/firmata) is a JavaScript library for the Arduino implementaion of firmata.

## Adapters

Finally, some frameworks implement _adapters_ to language-specific _libraries_.

## Firmata Software: All Together Now

1. The _firmata_ protocol
2. An _implementation_ of the firmata protocol for a platform (e.g. Arduino firmata)
3. A language-specific _library_ for an implementation (e.g. firmata.js)
4. (Sometimes) _adapters_ between software frameworks and _libraries_ (e.g. `cylon-firmata`)

_Example_: [`cylon-firmata`](https://github.com/hybridgroup/cylon-firmata) is an _adapter_ between the [`cylon.js`](http://cylonjs.com/) framework and the _[Firmata.js](https://github.com/jgautier/firmata)_ JavaScript _library_ for the [Arduino _implementation_](https://github.com/firmata/arduino) of the [firmata _protocol_](https://github.com/firmata/protocol). Whew!

*Note*: The popular [`johnny-five`](https://github.com/rwaldron/johnny-five) Node.js framework is also built on top of `firmata.js`.

## Firmata Firmware

To prepare hardware to be firmata-compatible, the microcontroller (or other processor) is flashed with _firmware_ that implements the firmata protocol.

For example, you can use the Arduino IDE to _flash_ (upload) firmata firmware to an Arduino's microcontroller. In fact, several different firmata _sketches_ come pre-packaged with the Arduino IDE.

Now both ends (software and hardware) are ready to communicate using the firmata protocol.
