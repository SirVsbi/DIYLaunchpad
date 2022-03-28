# DIY Launchpad design doc. nr 1 



## Software 

### Sound generation/manipulation 

- https://wiki.python.org/moin/Audio
  Sound library for python, which can be run on a raspberry pi 
  
- [Pyo](http://ajaxsoundstudio.com/software/pyo/)
  
  - [Pyo docs](http://ajaxsoundstudio.com/pyodoc/)
    - Great for sound generation. Also can load and play sound files
  
  Well, Pyo is out of the picture now. Can't make it run on own systems. 
  
- [Tone.Js](https://tonejs.github.io/)

  - Great js based library for sound generation/manipulation. It uses notes as a base unit. Although this solution increases the width of the tech stack, it's a way easier route to implement. 
  - Example tech stack: headless browser running node.js <-> python rest api <-> i/o devices 
  - This way the raspberry pi handles the sound output (bluetooth/3.5mm jack) and runs the REST api that can be used to program the launchpad 
  - Possible clients for the rest api: 
    - app written in flutter that can be run on phone/browser 
    - cli 

  - Firebase for auth/user handling 
  - Flexible design: just provide the different sound outputs (sinks) and the inputs (either the launchpad, keyboard, web interface, etc)
  - User sessions stored in cloud (this including auth, sounds etc)

