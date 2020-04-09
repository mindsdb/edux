# MindsDB eduX

EduX is a custom theme for Open edX, that follows MindsDB style guides.

## EduX Directory 

EduX directory mirrors the assets in the [openedx](https://github.com/edx/edx-platform/tree/master/themes) platform. All of the files must be used in the same place, and with the same name as the files in openedx platform.
```
edux
└── lms
    ├── static
    │   ├── images
    │   │   └── logo.png
    │   └── sass
    │       ├── _overrides.scss
    │       └── lms-main.scss
    └── templates
        ├── footer.html
        └── header.html
   cms
    ├── static
    │   ├── images
    │   │   └── logo.png
    │   └── sass
    │       ├── _overrides.scs
    └── templates
        ├── footer.html
```

# Installing eduX
1. First clone the eduX repository:
```sh
git clone https://github.com/mindsdb/edux
```
2. Add the theme inside openedx themes directory:
```sh
tutor config render  /edux "$(tutor config printroot)/env/build/openedx/themes/edux"
```
3. Re build the docker image:
```sh
tutor images build openedx
```
4. Restart cms and lms:
```sh
tutor local start -d
```
5. Login to admin panel `http://localhost/admin` and add site theme(theme-dir-name should be edux). 
