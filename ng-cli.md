# Angular CLI
* Follows best practices out of the box

### Installation
* Dependencies ***Node***, ***npm***

```bash
npm install -g @angular/cli
```

* verify

```bash
>> ng -v

### Ascii art
@angular/cli: 1.3.2
node: 8.2.1
os: darwin x64
```

### Generate an app
```bash
>> ng new ngtest --skip-install
# output
>> cd ngtest
>> ls
README.md		karma.conf.js		protractor.conf.js	tsconfig.json
e2e			package.json		src			tslint.json
```

* All of these files are configured automatically, `--skip-install` flag skips the npm install on the dependency list

### Commands
* new project : `ng new app-name`

* generate <blueprint> : `ng generate <blueprint> name`

  * blueprint types:

    * service
    * class (ts class)
    * component
    * pipe
    * directive
    * module

  * `ng g c customer` - generate a component named "customer"

    * auto updates appModule

  * `--flat true` - generate without a surrounding directory

  * `--spec false` - do not generate tests

* run on 4200 : `ng serve`

### Routing
* `ng new routing-app --routing`

* Provides `app-routing.module.ts`

* add `<router-outlet></router-outlet>` like ngView

* Add objects with `path` and `component` properties to load appropriate component

  * other properties:

    * `pathMatch` - 'full'
    * `redirectTo` - other path

* use `[routerLink]="['/pathName']"` and assign them to links as in:

```html
<a href="" [routerLink]="['/home']">Home</a>
```

### Builds
* Creates dist directory with bundled source code

* `ng build -aot` - use this for production, it reduces size of vendor bundle (pulls out the angular compiler)

* `ng build --prod` - includes aot and uglification, reduces overall size by ~80%.

### Serving an app
* `ng serve -o` open in browser

* `ng serve -p` set port

* `ng serve -lr` live reload

* `ng serve --prod -o`
