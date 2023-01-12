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
	
2. HTML:
	```html
	<main>  
	<nav style="--count: 4;">
		<ul>
		<li style="--index: 1;">
			<a href="#" target="_blank" rel="noreferrer noopener">
			<span><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
	<path stroke-linecap="round" stroke-linejoin="round" d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" />
	</svg>
	Socials</span>
			</a>
		</li>
		<li style="--index: 2;">
			<a href="https://twitter.com/jh3yy" target="_blank" rel="noreferrer noopener">
			<span>
				<svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>Twitter</title><path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/></svg>
				Twitter
			</span>
			</a>
		</li>
		<li style="--index: 3;">
			<a href="https://front-end.social/jhey" target="_blank" rel="noreferrer noopener">
			<span>
				<svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>Mastodon</title><path d="M23.268 5.313c-.35-2.578-2.617-4.61-5.304-5.004C17.51.242 15.792 0 11.813 0h-.03c-3.98 0-4.835.242-5.288.309C3.882.692 1.496 2.518.917 5.127.64 6.412.61 7.837.661 9.143c.074 1.874.088 3.745.26 5.611.118 1.24.325 2.47.62 3.68.55 2.237 2.777 4.098 4.96 4.857 2.336.792 4.849.923 7.256.38.265-.061.527-.132.786-.213.585-.184 1.27-.39 1.774-.753a.057.057 0 0 0 .023-.043v-1.809a.052.052 0 0 0-.02-.041.053.053 0 0 0-.046-.01 20.282 20.282 0 0 1-4.709.545c-2.73 0-3.463-1.284-3.674-1.818a5.593 5.593 0 0 1-.319-1.433.053.053 0 0 1 .066-.054c1.517.363 3.072.546 4.632.546.376 0 .75 0 1.125-.01 1.57-.044 3.224-.124 4.768-.422.038-.008.077-.015.11-.024 2.435-.464 4.753-1.92 4.989-5.604.008-.145.03-1.52.03-1.67.002-.512.167-3.63-.024-5.545zm-3.748 9.195h-2.561V8.29c0-1.309-.55-1.976-1.67-1.976-1.23 0-1.846.79-1.846 2.35v3.403h-2.546V8.663c0-1.56-.617-2.35-1.848-2.35-1.112 0-1.668.668-1.67 1.977v6.218H4.822V8.102c0-1.31.337-2.35 1.011-3.12.696-.77 1.608-1.164 2.74-1.164 1.311 0 2.302.5 2.962 1.498l.638 1.06.638-1.06c.66-.999 1.65-1.498 2.96-1.498 1.13 0 2.043.395 2.74 1.164.675.77 1.012 1.81 1.012 3.12z"/></svg>
				Mastodon
			</span>
			</a>
		</li>
		<li style="--index: 4;">
			<a href="https://codepen.io/jh3y" target="_blank" rel="noreferrer noopener">
			<span>
					<svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>CodePen</title><path d="M18.144 13.067v-2.134L16.55 12zm1.276 1.194a.628.628 0 01-.006.083l-.005.028-.011.053-.01.031c-.005.016-.01.031-.017.047l-.014.03a.78.78 0 01-.021.043l-.019.03a.57.57 0 01-.08.1l-.026.025a.602.602 0 01-.036.03l-.029.022-.01.008-6.782 4.522a.637.637 0 01-.708 0L4.864 14.79l-.01-.008a.599.599 0 01-.065-.052l-.026-.025-.032-.034-.021-.028a.588.588 0 01-.067-.11l-.014-.031a.644.644 0 01-.017-.047l-.01-.03c-.004-.018-.008-.036-.01-.054l-.006-.028a.628.628 0 01-.006-.083V9.739c0-.028.002-.055.006-.083l.005-.027.011-.054.01-.03a.574.574 0 01.12-.217l.031-.034.026-.025a.62.62 0 01.065-.052l.01-.008 6.782-4.521a.638.638 0 01.708 0l6.782 4.521.01.008.03.022.035.03c.01.008.017.016.026.025a.545.545 0 01.08.1l.019.03a.633.633 0 01.021.043l.014.03c.007.016.012.032.017.047l.01.031c.004.018.008.036.01.054l.006.027a.619.619 0 01.006.083zM12 0C5.373 0 0 5.372 0 12 0 18.627 5.373 24 12 24c6.628 0 12-5.372 12-12 0-6.627-5.372-12-12-12m0 10.492L9.745 12 12 13.51 14.255 12zm.638 4.124v2.975l4.996-3.33-2.232-1.493zm-6.272-.356l4.996 3.33v-2.974l-2.764-1.849zm11.268-4.52l-4.996-3.33v2.974l2.764 1.85zm-6.272-.356V6.41L6.366 9.74l2.232 1.493zm-5.506 1.549v2.134L7.45 12Z"/></svg>
				CodePen
			</span>
			</a>
		</li>
		</ul>
	</nav>
	</main>
	```