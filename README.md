# sample-web-server
テクノロジー（藤原）Node.jsによるサンプルWebサーバ

```
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3'
[{"breeds":[],"id":"ii","url":"https://cdn2.thecatapi.com/images/ii.jpg","width":591,"height":720},{"breeds":[],"id":"l1","url":"https://cdn2.thecatapi.com/images/l1.jpg","width":675,"height":1024},{"breeds":[],"id":"2qo","url":"https://cdn2.thecatapi.com/images/2qo.jpg","width":398,"height":500}]urasoutennoMacBook-Pro:sample-web-server urasouma$ brew install jq
Updating Homebrew...
==> Auto-updated Homebrew!
Updated 1 tap (homebrew/core).
==> New Formulae
scala@2.12                               swig@3
==> Updated Formulae
pyenv ✔             folly               librealsense        scons
armadillo           gibo                libsigc++           scrcpy
atlantis            glib                lmod                serverless
aws-sdk-cpp         glooctl             macvim              ship
bitrise             gmic                mesa                sops
braid               go                  mighttpd2           telegraf
calicoctl           godep               minio               terraform
certbot             graph-tool          minio-mc            terragrunt
cfn-lint            gst-plugins-good    nomad               tokei
chakra              helmfile            opa                 topgrade
circleci            hlint               paket               vultr
citus               imagemagick         pandoc              webpack
doctl               imagemagick@6       phpunit             whois
encfs               jdupes              procs               wildfly-as
envconsul           jfrog-cli-go        pulumi              wtf
exiftool            jhipster            pybind11            yelp-tools
firebase-cli        joplin              rbspy               you-get
flow                knot                scala
fluxctl             libev               scalariform
==> Deleted Formulae
scala@2.10                               swig@3.04

==> Installing dependencies for jq: oniguruma
==> Installing jq dependency: oniguruma
==> Downloading https://homebrew.bintray.com/bottles/oniguruma-6.9.2.mojave.bott
==> Downloading from https://akamai.bintray.com/c6/c613befafe81da48913ebd1a7eb03
######################################################################## 100.0%
==> Pouring oniguruma-6.9.2.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/oniguruma/6.9.2: 17 files, 1.3MB
==> Installing jq
==> Downloading https://homebrew.bintray.com/bottles/jq-1.6.mojave.bottle.1.tar.
==> Downloading from https://akamai.bintray.com/71/71f0e76c5b22e5088426c971d5e79
######################################################################## 100.0%
==> Pouring jq-1.6.mojave.bottle.1.tar.gz
🍺  /usr/local/Cellar/jq/1.6: 18 files, 1MB
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3' | jq
[
  {
    "breeds": [],
    "id": "a85",
    "url": "https://cdn2.thecatapi.com/images/a85.jpg",
    "width": 560,
    "height": 430
  },
  {
    "breeds": [],
    "id": "dcn",
    "url": "https://cdn2.thecatapi.com/images/dcn.jpg",
    "width": 576,
    "height": 1024
  },
  {
    "breeds": [],
    "categories": [
      {
        "id": 14,
        "name": "sinks"
      }
    ],
    "id": "MTc5MjcyOQ",
    "url": "https://cdn2.thecatapi.com/images/MTc5MjcyOQ.jpg",
    "width": 480,
    "height": 640
  }
]

```


```
499   cd fujiwara
  500  git clone git@github.com:wec-tech-app2019/sample-web-server.git
  501  cd sample-web-server/
  502  code .
  503  curl --silent --request GET --url https://api.thecatapi.com/v1/images/search
  504  curl --silent --request GET --url https://api.thecatapi.com/v1/images/search
  505  curl --silent --request GET --url https://cdn2.thecatapi.com/images/MTk0MDQwNQ.jpg
  506  curl --silent --request GET --url 'https://cdn2.thecatapi.com/images/MTk0MDQwNQ.jpg'
  507  curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3'
  508  clear
  509  curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3'
  510  brew install jq
  511  curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3' | jq
  512  history


```

```
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3' > thecat.json
-bash: thecat.json: Permission denied
urasoutennoMacBook-Pro:sample-web-server urasouma$ ls
README.md
urasoutennoMacBook-Pro:sample-web-server urasouma$ pwd
/Users/urasouma/fujiwara/sample-web-server
urasoutennoMacBook-Pro:sample-web-server urasouma$ ls -ld
drwxr-xr-x  5 urasouma  staff  160  6 14 09:45 .
urasoutennoMacBook-Pro:sample-web-server urasouma$ ls
README.md
urasoutennoMacBook-Pro:sample-web-server urasouma$ touch thecat.json
urasoutennoMacBook-Pro:sample-web-server urasouma$ ls
README.md	thecat.json
urasoutennoMacBook-Pro:sample-web-server urasouma$ rm thecat.json 
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3'
[{"breeds":[],"id":"dma","url":"https://cdn2.thecatapi.com/images/dma.png","width":697,"height":577},{"breeds":[],"id":"MTY0NTk1MQ","url":"https://cdn2.thecatapi.com/images/MTY0NTk1MQ.jpg","width":800,"height":600},{"breeds":[{"weight":{"imperial":"5 - 10","metric":"2 - 5"},"id":"tang","name":"Turkish Angora","cfa_url":"http://cfa.org/Breeds/BreedsSthruT/TurkishAngora.aspx","vetstreet_url":"http://www.vetstreet.com/cats/turkish-angora","vcahospitals_url":"https://vcahospitals.com/know-your-pet/cat-breeds/turkish-angora","temperament":"Affectionate, Agile, Clever, Gentle, Intelligent, Playful, Social","origin":"Turkey","country_codes":"TR","country_code":"TR","description":"This is a smart and intelligent cat which bonds well with humans. With its affectionate and playful personality the Angora is a top choice for families. The Angora gets along great with other pets in the home, but it will make clear who is in charge, and who the house belongs to","life_span":"15 - 18","indoor":0,"alt_names":"Ankara","adaptability":5,"affection_level":5,"child_friendly":4,"dog_friendly":5,"energy_level":5,"grooming":2,"health_issues":2,"intelligence":5,"shedding_level":2,"social_needs":5,"stranger_friendly":5,"vocalisation":3,"experimental":0,"hairless":0,"natural":1,"rare":0,"rex":0,"suppressed_tail":0,"short_legs":0,"wikipedia_url":"https://en.wikipedia.org/wiki/Turkish_Angora","hypoallergenic":0}],"id":"xTo8K7wb3","url":"https://cdn2.thecatapi.com/images/xTo8K7wb3.jpg","width":10
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3' > thecat.json
-bash: thecat.json: Permission denied
urasoutennoMacBook-Pro:sample-web-server urasouma$ which bash
/bin/bash
urasoutennoMacBook-Pro:sample-web-server urasouma$ pwd
/Users/urasouma/fujiwara/sample-web-server
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3' > thecat.json
-bash: thecat.json: Permission denied
urasoutennoMacBook-Pro:sample-web-server urasouma$ curl --silent --request GET --url 'https://api.thecatapi.com/v1/images/search?limit=3' > thecat.json
urasoutennoMacBook-Pro:sample-web-server urasouma$ 

```