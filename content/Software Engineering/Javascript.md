Upgrade pnpm through corepack:
	`corepack use pnpm@latest`

All JS Engines: https://github.com/ivankra/javascript-zoo
JS Runtimes: https://github.com/errilaz/awesome-js-runtimes?tab=readme-ov-file#runtimes

##### Context vs Scope
\[To add a way better example\]
This example is from [[ZTM Notes#Section 6 – Data structures Arrays]] (Optional: Classes in Javascript)

```javascript
function a() {
	console.log(this)
}

const my_obj = {
	a: function() {
		console.log(this)
	}
}
a()
my_obj.a()
```
##### Class
This example is from [[ZTM Notes#Section 6 – Data structures Arrays]] (Optional: Classes in Javascript)
```javascript
class Player {
	contructure(name, type) {
		console.log(this)
		this.name = name
		this.type = type
	}
	introduce() {
		console.log(`Hi I am ${this.name}, I'm a ${this.type}`)
	}
}

class Wizard extends Player {
	constructor(name, type) {
		super(name, type)
	}
	play() {
		console.log(`WEEEE I'm a ${this.type}`)
	}
}

const wizard1 = new Wizard('Shelly', 'Healer')
const wizard2 = new Wizard('Shawn', 'Dark Magic')
```