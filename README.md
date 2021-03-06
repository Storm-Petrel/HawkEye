<a href="https://storm-petrel.github.io/site/"><img src="https://raw.githubusercontent.com/Storm-Petrel/Hermes/master/Media/logo.png" title="Hermes" alt="Hermes"></a>

# Hermes

> A Storm Petrel Project aiming to build a geofence monitoring program for cars.

> Keeping you safe.

> geofence, car, security.

<img src="https://raw.githubusercontent.com/Storm-Petrel/Hermes/master/Media/hermes.gif" title="Idea" alt="idea" height="500" width="600">

***Implementation***

For this project to work there is a need for the use of the code in this repository, and besides the code there is also a need to create node-red and cloudant instances in the IBM Bluemix for signaling.
![Bluemix](https://github.com/Storm-Petrel/Hermes/blob/master/Media/node-red.png)

***Description***

Every car can have multiple geofences and the one that's active is based on the car's current position.
Every time the car leaves it's active geofence an alert is emitted to a Security Central. The Central then checks if it's really an
alert situation, in the case the alert is real the Central will ask for an user password (currently in an Arduino).
Every user will have two passwords, a "safe" one, that deactivates the alert and creates a temporary fence, and an "emergency" one.
If the input is equal to the emergency password, the "safe" password is not typed in 5 minutes or if the user types a wrong password
4 times, an email is emitted to the Central asking it to talk with the authorities.

# Security Central
If you want to implement this project you need to create two emails for the security central, one to emit the alerts and one to receive them and see if it is necessary to ask for the user to input his passwords.

>The Security Central, first receives the alert email and verifies if it is necessary to ask the user for his passwords.
![Central Alert](https://raw.githubusercontent.com/Storm-Petrel/Hermes/master/Media/Central-Alerta.gif)

>If the user's input is equal to emergency the Security Central receives an email asking it to contact the authorities.
![Central Authorities](https://raw.githubusercontent.com/Storm-Petrel/Hermes/master/Media/Central-Autoridades.gif)

# Temporary Fence
If the user's input is the "safe" password a temporary geofence, with the duration of 24 hours is generated, after this period is over the fence returns to it's original form.

![Temporary Fence](https://raw.githubusercontent.com/Storm-Petrel/Hermes/master/Media/temporary-fence.gif)

**CODE**

![Recordit GIF](http://g.recordit.co/Rw5bXM5S20.gif)


## Team

| <a href="https://github.com/Beatr1z" target="_blank">**Beatriz Sérvio**</a> | <a href="https://github.com/joaovictor1020" target="_blank">**João Victor Bravo**</a> | <a href="https://github.com/leon13344" target="_blank">**Leonardo Rodrigues**</a> |
| :---: |:---:| :---:|
| [![FVCproductions](https://avatars1.githubusercontent.com/u/40302576?v=3&s=200)](https://github.com/Beatr1z)    | [![FVCproductions](https://avatars0.githubusercontent.com/u/39501506?v=3&s=200)](https://github.com/joaovictor1020) | [![FVCproductions](https://avatars3.githubusercontent.com/u/40325429?v=3&s=200)](http://fvcproductions.com)  |
| <a href="https://github.com/Beatr1z" target="_blank">`https://github.com/Beatr1z`</a> | <a href="https://github.com/joaovictor1020" target="_blank">`https://github.com/joaovictor1020`</a> | <a href="https://github.com/leon13344" target="_blank">`https://github.com/leon13344`</a> |

| <a href="https://github.com/polesi" target="_blank">**Mariana Polesi**</a> | <a href="https://github.com/m4th21" target="_blank">**Matheus Farias**</a> | <a href="https://github.com/tiagovalenca" target="_blank">**Tiago Valença**</a> |
| :---: |:---:| :---:|
| [![FVCproductions](https://avatars2.githubusercontent.com/u/40322420?v=3&s=200)](http://fvcproductions.com)    | [![FVCproductions](https://avatars0.githubusercontent.com/u/38105118?v=3&s=200)](https://github.com/m4th21) | [![FVCproductions](https://avatars2.githubusercontent.com/u/36921610?v=3&s=200)](https://github.com/tiagovalenca)  |
| <a href="https://github.com/polesi" target="_blank">`https://github.com/polesi`</a> | <a href="https://github.com/m4th21" target="_blank">`https://github.com/m4th21`</a> | <a href="https://github.com/tiagovalenca" target="_blank">`https://github.com/tiagovalenca`</a> |

---

## Contact

Reach us at one of the following places!

- Website at <a href="https://storm-petrel.github.io/site/" target="_blank">`storm-petrel.github.io/site/`</a>
- Facebook at <a href="https://www.facebook.com/CSStormPetrel/" target="_blank">`@CSStormPetrel`</a>


## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2018 © <a href="https://storm-petrel.github.io/site/" target="_blank"> `Storm Petrel`</a>.
