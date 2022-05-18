### GPS Drivers ###


### Use Galileo OSNMA
Open Service Navigation Message Authentication (OSNMA) is a data authentication function for the Galileo Open Service worldwide users, freely accessible to all. OSNMA provides receivers with the assurance that the received Galileo navigation message is coming from the system itself and has not been modified.

In Septentrio receivers, OSNMA is used to discard untrusted satellites from the PVT computation. Three operating modes are supported: off where OSNMA authentication is disabled,
loose where satellites are included in the PVT if they are successfully authenticated or if their
authentication status is unknown, and strict where only successfully-authenticated satellites
are included in the PVT.

In strict mode, the number of satellites available to the PVT may be limited as OSNMA does
not authenticate all visible satellites (e.g. only Galileo and GPS satellites depending on the
OSNMA service status).

After enabling OSNMA (in loose or strict mode), it typically takes a few tens of seconds to
a few minutes to authenticate messages. In strict mode, no PVT is computed during that time.

The receiver has been optimized for use with live Galileo signals. Necessary keys are embedded into the software. For example the Galileo Merkle Tree root key, needed to enable
over-the-air reception of public keys, is known by the receiver, obviating the need for the user
to provide it.


* More info about spoofing and jamming in general: https://www.septentrio.com/en/company/septentrio-gnss-technology/advanced-interference-monitoring-mitigation-aim
* More info on OSNMA: https://www.gsc-europa.eu/galileo/services/galileo-open-service-navigation-message-authentication-osnma

