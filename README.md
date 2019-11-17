README.md

# Possible Component Queries Bug When Running Ivy In Non-Production Mode In Angular 9.0.0-rc.2

This is an isolated repository for a potential bug in Ivy - or something that interacts with Ivy - in the development server provided by the Angular CLI. This project has only two run-scripts:

```json
"scripts": {
	"start-dev": "ng serve --open",
	"start-prod": "ng serve --open --prod"
},
```

If you run this using `npm run start-dev`, you get the following output:

<p align="center">
	<img src="./start-dev-screenshot.png?raw=true" style="display: inline-block ; border: 5px solid #cccccc ;" />
</p>

And, if you run this using `npm run start-prod`, you get the following output:

<p align="center">
	<img src="./start-prod-screenshot.png?raw=true" style="display: inline-block ; border: 5px solid #cccccc ;" />
</p>

As you can see, in the `dev` mode, only the `@ViewChild()` property annotation works. However, in the `prod` mode, both approaches work.
