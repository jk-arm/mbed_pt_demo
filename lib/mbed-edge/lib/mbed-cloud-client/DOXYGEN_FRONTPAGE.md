## Device Management Client API

This is the Doxygen-generated API documentation for Device Management Client. See the [Files](files.html) section to find the documentation about a specific API. You should also use the [Device Management documentation](../connecting/index.html).

The Device Management Client high-level APIs allow developers to create client side applications that connect to **Device Management**, with LwM2M features as described in the [Lightweight Machine to Machine Technical Specification](http://www.openmobilealliance.org/release/LightweightM2M/V1_0-20170208-A/OMA-TS-LightweightM2M-V1_0-20170208-A.pdf).

Device Management Client is an extension of the existing [Mbed Client API](../mbed-client/index.html). It provides an additional feature of creating a unique identity for the client on the **Device Management** and also provides functionality to update the client's software through the **Device Management** service.

These APIs make it possible to:

- Use a factory flashed or developer credentials to create a unique device identity.
- Securely communicate with internet services over the industry standard TLS/DTLS.
- Manage devices.
- Fully control the endpoint and application logic from the service side. 
- Provide functionality to update the devices over the air remotely controlled from the service side.
- Have a unified porting layer for porting to different platforms.

The API is in C++ to allow quick application development.
