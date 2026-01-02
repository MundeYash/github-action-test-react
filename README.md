Steps to set-up Github Action (CI-CD )tool with react project

Step1: first Add Node.js format yaml to git-repository

Step2: copy content of Node.js.yaml to that file and commit the changes.

Step3: update the package json with

    homepage attribute under private attribute,
        "homepage": "https://usernameofgithub.github.io/repositorynameofgithub/",


     add deploy attribute under scripts,
        "deploy": "gh-pages -d dist",


     add git pages attribute under devDependecies
        "gh-pages": "^6.3.0",


Step4 : inside vite.config.ts file add
base:"/github-action-test-react"

Step5:

in yaml file give permission

      permissions:
    contents: write

and add working directory path where package.json is present

      defaults:
      run:
        working-directory: nameoffolderworkingdirectory

Step6: change the branch to gh-pages via going into setting of github repo under pages section. reload the build and move the url

It will work as expected
