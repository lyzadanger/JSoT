**I^2C** or **I2C** (Inter-Integrated Circuit), pronounced _eye-squared-see_ or _eye-two-see_, is a common communication protocol that requires only 2 lines, _Data_ (**SDA**) and _Clock_ (**SCL**).

Compared to SPI communication, where a unique _Slave_Select_ line is needed for each additional connected device, I2C-compatible devices can all connect to these same two lines in parallel. This means only 2 pins are needed from a _master_ (e.g. microcontroller) to communicate to over 100 other _slave_ devices such as sensors, EEPROMs, and even other microcontrollers. There are also more advanced implementations available.

I2C communication does have limitations. Each connected _slave_ device on a shared bus (pair of I2C lines, SDA and SCL) must have a unique, 7-bit address. These can be programmed (such as in the case of another microcontroller acting as a _slave_), configured by connecting certain available pins to power or ground, or factory set (permanent). The data rate can be slower than some other methods, such as SPI, but it's often more than enough for most applications.

One important detail about the implementation of I2C is that the two shared bus lines must also be connected to the shared power source through resistors (pullup resistors). The value for these resistors may depend on the length of the bus and the number of devices connected, but 10k ohms is fairly standard.

I2C was once a proprietary technology. Other companies created similar and compatible bus communications, such as Two-Wire Interface (TWI). Typically, if there are a pair of **SDA** and **SCL** pins, then the device usually supports _some_ form of I2C.
