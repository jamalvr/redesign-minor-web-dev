# Website redesign for the minor Web Development

During this project we redesigned the website for the minor 'web development' at the University of Applied sciences in Amsterdam. We have done our best to make a very experimental yet pleasurable web site.

A big theme in this project was 'accessibility'. The site should be pleasurable for everyone, not just for the 'general public'.

## Persoonlijke Readme

Zelf heb ik voor deze eindopdracht gekozen omdat dit mij de leukste opdracht leek om styling en functionaliteit samen te kunnen voegen. Vanuit mijn eigen ervaring waren er ook delen informatie die voor mij onduidelijk waren voordat ik aan de minor begon. Het lijkt mij daarom een goede uitdaging om er voor te zorgen dat toekomstige studenten complete informatie kunnen vinden.

We hebben eerst met z’n allen gezeten en besloten dat we de opdracht in teamvorm gaan uitvoeren. Om er voor te zorgen dat wel iedereen aan zijn persoonlijke leerdoelen komt, hebben we die eerst met z’n allen besproken. Aan de hand van de leerdoelen die iedereen opnoemde, kwamen we al snel tot de conclusie dat we elkaar heel goed kunnen aanvullen en helpen.

### Leerdoelen & uitdagingen

#### Grootste uitdagingen:

- Strakke planning aanhouden.
- Goed in kaart brengen wat een gebruiker echt nodig heeft. \* Eerst een ijzersterk concept voordat ik met de uitwerking begin.

#### Leerdoelen

- Combineren van styling & functionaliteit.
- Schrijven van nette code.
- Beter leren plannen.

#### Afleer doelen

- Bang om eventueel functionaliteiten niet toe te voegen omdat het niveau te hoog is / code te ingewikkeld wordt.
- Omdat je uitgebreid styling en functionaliteit kan toevoegen en ook van waarde kan zijn voor de minor zelf.

#### Over de leerdoelen

Ik ben van mezelf (nog) geen pro-programmeur, dus ik wil mezelf graag uitdagen om ook functioneel aan de slag te gaan met de website. Ik heb gelukkig al wel design skills en wil dit kunnen combineren met functionaliteit. Omdat ik met meerdere mensen in een groepje zit, wil ik graag gebruik maken van de kans om samen aan code te worden zodat we van elkaar kunnen leren.

- **[Pull requests van Jamal](https://github.com/baskager/redesign-minor-web-dev/pulls?utf8=%E2%9C%93&q=author%3Ajamalvr+)**

### Conclusie

Wat ik voornamelijk heb gemerkt is dat het heel belangrijk is om goed na te denken over hoe je het project gaat opzetten. Het grootste struikelblok is dan toch juist in teams werken. We liepen bijvoorbeeld al snel tegen verschillende codestylen aan en toch stiekem best wel wat onnodige bugs/merg conflicts. Er werden daardoor heel vaak kleine fixes dubbel gedaan.

Ook is het belangrijk om toch een project qua scope goed in te kunnen schatten en ook beter na te denken over wat de gebruiker wilt. Zo is er bijvoorbeeld relatief erg veel tijd gestopt in het opzetten van een database, terwijl het niet perse nodig is en misschien ook helemaal niet handig is voor de leraren. Al met al werkt het overigens wel goed met de database, maar toch komen er altijd extra dingen bij kijken. Het was niet perse slecht, maar wel een kritisch puntje om over na te denken.

Verder vond ik het zelf echt super vet om samen te werken. Zelf vind ik dat ook de leukste manier van werken, omdat je super veel inzichten van elkaar krijgt. Mensen snappen ook beter waar ik mee bezig ben omdat je in hetzelfde project werk, wat het weer makkelijker maakt om de juist hulp te vragen. Hierdoor heb ik bijvoorbeeld best veel stappen kunnen maken in het zelfstandig schrijven van javascript.

De code werd ook regelmatig gecheckt door iemand anders. Gelukkig was iedereen kritisch genoeg om feedback te geven wanneer er iets niet klopt of anders gedaan kan worden. Dit maakte het makkelijk om ook van elkaar te leren en elkaars code conventies te snappen. Bijvoorbeeld dat het handig is in SASS om niet dieper dan 3 niveaus te gaan, omdat je anders hele specifieke code krijgt die tegelijkertijd zwaarder wordt door de lange selectors.

Los van het soms moeilijk kunnen inschatten van prioriteiten, ging de planning best wel soepel. Meerdere keren per week werd er geïnventariseerd wat er allemaal gedaan moest worden. Vervolgens werden de verschillende taken onder elkaar verdeeld. Hierdoor werden de taken ongeveer gelijk verdeeld, was het duidelijk voor iedereen wat die moest doen en konden we makkelijk rekening houden met elkaars leerdoelen.

## Team Readme

![Homepage](https://d.pr/i/DuFm0H+)

[Demo here!](https://redesign-minor.kager.io/)

# 1. Requirements

- NPM (node package manager)
- NodeJS
- GULP (task-runner)
- Browserify

# 2. Installing and building

## Clone this repository

```
git clone git@github.com:baskager/redesign-minor-web-dev.git
```

## Navigate to the `/app` directory and run NPM install

This will install all the NPM packages that are used throughout the project.

```
cd app
npm install
```

# 3. Deploying on development

## Checkout to the develop branch

```
git checkout develop
```

## Run gulp watch

This will check for changes in the assets and run the gulp task runner when needed.

```
gulp watch
```

## Start the server

We recommend using Nodemon for development. This will restart the server when the code is changed. The will also run the server on http://localhost:3000.

```
npm install -g nodemon
nodemon server.js
```

# 4. Deploying on production

## Install forever on the server.

Forever will run the server continuously and detached

```
npm install -g forever
```

## Run gulp

This will compile all the assets

```
gulp
```

## Run forever and let it write logs in the `/logs` folder.

```
forever -o logs/node-server-out.log -e logs/node-server-error.log start app.js
```

# 5. Experiments

## 'Hector Salamanca' input method by Rick

Rick made a very experimental version of a keyboard that ( according to his research ) shoud be very accessible for Marijn. Check out [his progress Blog](https://github.com/baskager/redesign-minor-web-dev/blob/develop/docs/process/rick.md) for the full research and results of the test with Marijn.

## Video element with captions and split screen

For deaf people it is hard to follow lectures. They have to focus on the speaker, the interpreter and the slides at the same time. As we are making a website for a minor lectures are part of it. To make it easier for deaf people to follow the lectures I made a video player focused on improving this experience. We tested the video player with Marie, a deaf graphic designer. She gave us a lot of interesting feedback. With this feedback we improved the video player to it's current form.

**The video player contains the following features:**

- Synced split screen view of the lecture and the slides
- Subtitles (loaded as SRT format).
- The subtitles can switch side using the mouse or arrow keys.
- Slide overview to quickly navigate trough the lecture
- The possibility to slowdown or speed up the lecture.
- The video player can be controlled using the keyboard.

![Screenshot of the videoplayer](https://d.pr/i/tQJ6Uu+)

## Spatial navigation on the program page

The spatial navigation functionality is deeply inspired by the original Opera function and by multiple large screen navigation systems. Users can easily navigate through elements using their arrow keys. Unlike the forward jumping tab key, users can navigate in any direction. The enter key will emulate the mouse's on click event. More information can be found on James personal progress [blog](https://jamerrone.github.io/meesterproef-progress-blog/).

## Focus following the scroll position

Marijn once told me that the biggest disadvantage of the tab key was the fact that it always starts at the top of the website. If the user chooses to scroll down the page and wants to interact with an element, he will need to spam the tab key until he get's there. With this functionality James wrote, the focus key will always follow the user's window location. The focus state will change its current element depending on what is currently displayed on the screen. More information can be found on James personal progress [blog](https://jamerrone.github.io/meesterproef-progress-blog/).

## Navigation through hotkeys

In our interviews/test with Marijn, he told us that he really liked interfaces dat can be used through hotkeys. Now, all the pages in the main menu are available when you use the keys with a number on it. Look at the number in de main navigation to know which number you have to press. This feature can be toggled on or off when you press alt + ctrl simultaniously. Every user should be able to navigate quickly through the website without too much effort. Especially in combination with the spacial navigation and focus on scroll position.

**How to use the hotkeys**

- If the indicator on the bottom right is transparent, press `control + alt` to toggle the hotkeys.
- With [1, 2, 3, 4, 5, 6] you can navigate through the different pages on the website.

![hotkeys](https://i.imgur.com/Yt4w2Wo.png)

## Spatial navigation slider element

# 6. Insights

The experiments were eye-opening for us as a team. Every member of the team represents the 'general public'. We use a computer and websites like most of society. Not often do we as developers realise our privileges and that leads to designing and developing things that might not be ideal for users that need/use additional accessibility features.

Testing and conversing with Marijn and Marie made us realise that the web/software is used in so many different ways and what for some is pleasurable can be an obstacle for others.

We found out that it is extremely difficult to make something pleasurable and accessible at the same time. It takes experiments, testing and a lot of iterations to get something right. It, however, is extremely useful and after a while it just makes sense.

When designing pleasurably accessible website elements you will find out that some designs are actually more pleasurable for the general public as well. There are some things we just get wrong in general and continuously testing helps us to realize this.

We highly recommend making websites/software more accessible if the time and money is available. You'll find out a lot of things that you can implement in future projects. Your finished work will have far more value because there are far more people that can use your product pleasurably. This isn't just financial value, it's also social value.

It really means something to the people who use it and we think that is powerful.

# 7. Conclusions

- Don't assume things are pleasurable for everyone. Test it with a diverse group of people, including people who need accessibility software like screen readers.
- Take your time to experiment and build prototypes, it's actually really fun and useful.
- We all have something to learn, even when we think we don't.

# 8. Roadmap

Write this when we sign off on the project

# 9. Versioning

We use semantic versioning. More information can be found on http://semver.org

# 10. License

We use the "MIT License"

> A short and simple permissive license with conditions only requiring preservation of copyright and license notices. Licensed works, modifications and larger works may be distributed under different terms and without source code.

You can find our license here: https://github.com/baskager/redesign-minor-web-dev/blob/master/LICENSE

# 11. Authors

## James Jefferies

![Profile photo](https://avatars3.githubusercontent.com/u/16142485?s=460&v=4)

Ex-Graphical Design student that refound himself as a Frontend Developer at the University of Applied Science Amsterdam.

[Github repo](https://github.com/Jamerrone)

[Progress Blog](https://jamerrone.github.io/meesterproef-progress-blog/)

## Jelle Overbeek

![Profile photo](https://avatars0.githubusercontent.com/u/6648715?s=460&v=4)

Designer that also likes to code.

[Github repo](https://github.com/jelleoverbeek)

[Progress Blog](https://github.com/baskager/redesign-minor-web-dev/blob/develop/docs/process/jelle.md)

## Rick Buter

![Profile photo](https://avatars1.githubusercontent.com/u/22095570?s=460&v=4)

Doesn't really know what he's doing, but he's doing just fine.

[Github repo](https://github.com/Rick712)

[Progress Blog](https://github.com/baskager/redesign-minor-web-dev/blob/develop/docs/process/rick.md)

## Jamal van Rooijen

![Profile photo](https://avatars3.githubusercontent.com/u/26875486?s=460&v=4)

A designer who just recently discovered his love for code.s

[Github repo](https://github.com/jamalvr)

[Jamal his progress blog](https://github.com/baskager/redesign-minor-web-dev/blob/develop/docs/process/jamal.md).

## Bas Kager

![Profile photo](https://avatars3.githubusercontent.com/u/5838517?s=460&v=4)

Software Engineer studying at The University of Applied Sciences Leiden. Really likes databases, performance, security and clean code.

[Github repo](https://github.com/baskager)

[Progress Blog]()

# 12. Acknowledgements

A very special thank you to Marijn and Marie for helping us with accessibility testing and the design process. This project would not have been possible without them.

We would also like the thank all the teachers for the guidance in this project but also in the entire minor. They really went out of their way to push us and teach us something new.

# 13. Individual goals for this project

**James Peter Perrone Jefferies:**

1.  Learn how to build and manage complex project structures, for example, components splitting, folder structure, and name conventions.
2.  Don't be afraid to try new stuff out, be creative, and build awesome stuff where users can say: WoW!
3.  Don't write "quick fixes" or "prototype code". Try to write good code from the startup. Because I know that I won't refactor it later.

**Jamal van Rooijen:**

1.  Learning how to plan properly in this project. Especially since we are with a team of five people. Dividing tasks and completing our personal goals can only be achieved by planning properly.
2.  Learning more Javascript by developing interactive elements on the website, without being afraid to try new and innovative things if it seems too 'hard' on first glance.
3.  Combining style and functionality, which should result in something that is pleasurable to use and has a 'Wow factor'.

**Rick:**

1.  Animations and Transitions that increase the user experience
2.  Clean code so that it is readable for everyone
3.  A bit design to improve my skills

**Bas Kager:**

1.  Learn how to build proper CSS layouts with flexbox, grid and best practices.
2.  Get up to speed with tasks runners.
3.  Learn more about web design (best) practices

**Jelle Overbeek:**

1.  Performance matters - Setting up a Node server including performance optimisations
2.  Web Design - Out of the box design, include more creativity than usual and try to deliver a wow experience.
3.  WAFS - General JavaScript knowledge, make efficient JavaScript functions.
