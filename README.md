# Outguess Docker container

An easy way to outguess stuff.

* Embed message.txt into original.jpg:

        $ cat message.txt
        all work and no play makes Jack a dull boy
        $ docker run -it --rm -v `pwd`:/data:Z sjourdan/outguess -d message.txt original.jpg destination.jpg

* Recover delivered.txt from destination.jpg:

        $ docker run -it --rm -v `pwd`:/data:Z sjourdan/outguess -r destination.jpg delivered.txt
        $ cat delivered.txt
        all work and no play makes Jack a dull boy

Enjoy.

Original `README` is the file `README`.
