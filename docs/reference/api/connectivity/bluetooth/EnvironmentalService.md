## EnvironmentalService

The Environmental Service exposes measurement data from an environmental sensor intended for sports and fitness applications. This implementation has a fixed set of characteristics: temperature, humidity and pressure.

The [Environmental Sensing Service](https://www.bluetooth.org/docman/handlers/downloaddoc.ashx?doc_id=294797) defines how data from sensors should be exposed through a BLE link. The standard nature of the service allows seamless operations between collectors (usually smartphone applications) and sensors conforming to the service.

This service creates three characteristics: temperature, humidity and pressure. It allows you to update them but multiplies the supplied values by arbitrary numbers (times a 100 for temperature and humidity and times 10 for pressure). The units are undefined. No characteristic descriptors describing measurements or allowing for configuration of triggers are present. This class is not extendible.

**Note:** The Bluetooth Environmental Sensing Service is part of the [Bluetooth Environmental Sensing Profile](https://www.bluetooth.org/docman/handlers/downloaddoc.ashx?doc_id=294796), which defines behaviours that a Bluetooth Environmental sensor expects.

### EnvironmentalService class reference

[![View code](http://os-doc-builder.test.mbed.com/docs/development/mbed-os-api-doxy/class_environmental_service.html)

### EnvironmentalService example

[Add example here.]
