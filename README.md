## HPC Users Group #4
This is a presentation I gave at the 4th HPC Users Group meeting at ILRI, Kenya. It's an informal group I created to encourage good practices amongst the users of ILRI's research computing platform.

![Screenshot](/screenshot@2x.png?raw=true "Screenshot")

You can view the presentation on GitHub Pages [here](https://alanorth.github.io/hpc-users-group4).

### Hacking
If you want to hack on this repo (ie for your own presentation) you will have to clone the repo and then initialize the reveal.js submodule:

    $ git submodule init
    $ git submodule update

Then create a Python virtual environment to setup the required tools for building the presentation:

    $ pyenv install 2.7.10
    $ pyenv virtualenv 2.7.10 reveal
    $ pyenv activate reveal
    $ pip install -r requirements.txt

After hacking on the slides in the `source/` directory, build the presentation and start a web server to serve the slides:

    $ fab build
    $ cd presentation
    $ python -m SimpleHTTPServer

The presentation will be available at [http://localhost:8000](http://localhost:8000).

### License
This repository contains the code of [reveal.js](https://github.com/hakimel/reveal.js) which is licensed under the [MIT license](https://github.com/hakimel/reveal.js/blob/master/LICENSE).

Otherwise, the contents of `source/` are licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
