# LC101 Unit 1 Javascript Web Development Course
- this is the react version of unit 1
- this is a fork of launchcode's original react version to to work better for an offline learning environment
- this repo creates the full static site which should be saved to s3
- then the https://github.com/unlockedlabs/unlockedos project will pull the compiled tarball down from s3 when an image is built

# Installation/Setup
- you need a specific version of hugo
` wget https://github.com/gohugoio/hugo/releases/download/v0.121.0/hugo_0.121.0_linux-amd64.deb `
` sudo dpkg -i hugo_0.121.0_linux-amd64.deb `

# Local Development
- `hugo serve`

# Deployment
```
hugo 
mv public javascript.education.launchcode.org
tar -czvf intro_to_web_dev_curriculum-0.0.1.tar.gz javascript.education.launchcode.org
aws s3 cp intro_to_web_dev_curriculum-0.0.1.tar.gz s3://debianimage/intro_to_web_dev_curriculum-0.0.1.tar.gz
```
