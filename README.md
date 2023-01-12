<div>
	<div>
		<img src=https://raw.githubusercontent.com/Byron2016/00_forImages/main/images/Logo_01_00.png align=left alt=MyLogo width=200>
	</div>
	&nbsp;
	<div>
		<h1>018_00_HTML_css_menuDesplegable</h1>
	</div>
</div>

&nbsp;

## Project Description

**DropRight.Web** is a practice ot the using of **CSS properties**. With css, following CodePen Jhey's example [grid-template links](https://codepen.io/jh3y/pen/MWBmmxb) and the other help that you can find into **Reference** section.
&nbsp;

## Steps
## Technologies used

![Sass](https://img.shields.io/static/v1?label=&message=sass&color=CC6699&logo=sass&logoColor=white&style=for-the-badge)
![CSS](https://img.shields.io/static/v1?label=&message=css&color=1572B6&logo=css3&logoColor=white&style=for-the-badge)


## References

- Sass
	- By Coder Coder
		-  [Sass, BEM y Responsive Design (curso para principiantes de 4 horas)](https://www.youtube.com/watch?v=jfMHA8SqUL4)

	- By Kevin Powel
		-  [Stop using an extension to compile Sass](https://www.youtube.com/watch?v=o4cECvhrBo8)

	- By Stephanie Eckles
		- [Minimum Static Site Setup with Sass](https://thinkdobecreate.com/articles/minimum-static-site-sass-setup/)


## Steps

1. Visual Studio Code:
	- Extensions
		- Sass
			- Live Sass Compiler (Compile Sass or Scss to CSS at realtime.)
				- Glenn Marks

			- Configuration
				- Into VSC press crtl + shift + p
				- Type: open settings
				- Choose: Preferences: Open Workspace Settings (JSON)
				```
				{
					"liveSassCompile.settings.formats": [
						{
							"format": "expanded",
							"extensionName": ".css",
							"savePath": "/src/css",
							"savePathReplacementPairs": null
						}
					]
				}
				```

		- Live Server (Launch a development local Server with live reload feature for static & dynamic pages)
			- Ritwick Dey
	- Extensions Alternatives
		- Create package.json file
		```
		npm init -y
		```
		- Add these scripts and modules
		```bash
		"scripts": {
			"copy:css": "copyfiles -u 1 ./src/css/**/*.css build/public",
			"copy:assets": "copyfiles -u 1 ./src/assets/**/* build/public",
			"copy:html": "copyfiles -u 1 ./src/*.html build/public",
			"copy": "npm-run-all --parallel copy:*",

			"build": "npm-run-all copy:* build:*",
			"postbuild": "postcss build/public/css/*.css -u autoprefixer cssnano -r --no-map"
			
		},
		"devDependencies": {
			"autoprefixer": "10.4.13",
			"copyfiles": "2.4.1",
			"cssnano": "5.1.14",
			"npm-run-all": "4.1.5",
			"postcss-cli": "10.1.0"
		},
		```
		- Create build's files
		```
		npm run build
		```