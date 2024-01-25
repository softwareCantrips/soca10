# Remove Karma and Jasmine

```
npm remove @types/jasmine jasmine-core karma karma-chrome-launcher karma-coverage karma-jasmine karma-jasmine-html-reporter
```
# Replace the test script:

```
"test": "jest",
"test:watch": "jest --watch",
"test:coverage": "jest --coverage",
```

# Install Jest

```
npm install --save-dev @types/jest jest-preset-angular
```

# jest.config.js

```
module.exports = {
  preset: 'jest-preset-angular',
  setupFilesAfterEnv: ['<rootDir>/src/setup.jest.ts'],
};
```

# tsconfig.spec.json

```
types ["jest", node]
"files": [
    "src/setup.jest.ts"
  ],
```

# setup.jest.ts

```
import 'jest-preset-angular/setup-jest';
```

# the sum function

```
sum(a: number, b: number) {
    return a + b;
}
```

# app.component.spec.ts

```
describe('AppComponent', () => {
  let fixture: AppComponent;
  beforeEach(() => {
    fixture = new AppComponent();
  });
  it('add two numbers', () => {
    expect(fixture.sum(1,4)).toBe(5);
  });
});
```

# Run the test

```
npm run test
```


# Soca10

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 17.0.8.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
