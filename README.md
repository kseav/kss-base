# kss-base
This is a basic setup for KSS (Knyle Style Sheets) built using kss-node.

How to use this Navigate to root directory of "kss-base" and run 'npm install'.
You will need node.js to be able to install packages using npm. Dependancies have already been set in package.json.

To compile KSS markdown (comments and html)
- npm run kss

To convert sass to css (sass only)
- npm run scss
	
Refer to these docos as a guide: https://css-tricks.com/build-style-guide-straight-sass/https://www.npmjs.com/package/kss https://github.com/kss-node/kss-node

Language agnostic: 
kss-node does not care what language your application is written in (Ruby, Node.js, PHP, whatever). It just scans your CSS source files looking for KSS docs so that it can build a living style guide. And since it only looks for properly formatted KSS comments, it also doesn't need to know what kind of CSS preprocessor you use either. This means that you will need to integrate it into your own task runner to perform tasks such as converting sass to css etc. You will no longer require kss-config.json in this case. We used webpack and utilised the kss-webpack-plugin.

Extra notes: 
This guide demonstrates two ways of presenting markup, within sass files and as a seperate html file. A "_markup" folder will need to be created as a subfolder under your sass folder. This is where your html files will live. Neither of the documentation above clearly specifies how to do this. You will also need to add a styleguide.md file under your sass folder. This will act as the your styleguide's homepage at /kss-base/styleguide/index.html.
