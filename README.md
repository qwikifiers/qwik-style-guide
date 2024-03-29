
# Qwik Style Guide

Coding style guides are usually written after years of experience, lessons learned and feedback from real and big projects using a specific technology.

[Qwik](https://qwik.builder.io/) is a new and revolutionary framework and because of that, many best practices are still being discovered as more Qwik apps are being built.

This guide is meant to serve as an ever evolving document, where best practices are being suggested, debated and added by Qwik community members.

The aim is to potentially "graduate" the most popular / agreed upon rules into the official Qwik docs and / or as rules for the Qwik ESLint plugin. 



<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Table of Contents

- [File Naming](#file-naming)
  - [Use kebab-case for files](#use-kebab-case-for-files)
- [Variables Naming](#variables-naming)
  - ["Sig" Suffix for Signals](#sig-suffix-for-signals)
- [Tasks](#tasks)
  - [Tasks named functions](#tasks-named-functions)
- [Translations](#translations)
- [Inspirations & Credits](#inspirations--credits)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

*generated with [DocToc](https://github.com/thlorenz/doctoc)*


## File Naming
### Use kebab-case for files

  - Use the kebab case for file names

#### Why? 🤔
To keep things consistent across the entire project.
  
This is not a must rule, but whatever convention you use, stick with it. 

  

#### Example

```typescript
/* avoid */

src/
  components/
    MyComponent.tsx

```

Pay attention to the file name below

```typescript
/* recommended */

src/
  components/
    my-component.tsx

```

## Variables Naming

### "Sig" Suffix for Signals

  - Use the `Sig` suffix for signals variable names

#### Why? 🤔
To make the component code more "Scannable" 
  
#### Example

```typescript
/* avoid */

const counter = useSignal(0);

```

Use the `Sig` suffix for signals variable names.

```typescript
/* recommended */

const counterSig = useSignal(0);
```

**[Back to top](#table-of-contents)**


## Tasks

### Tasks named functions

  - Use regular named functions instead of arrow functions for tasks and visible tasks.

#### Why? 🤔
When having several tasks inside a component, it's hard to understand what is each task doing without reading its implementation.

So having a regular function gives a name for the task describing its responsibility.

Plus, it helps when debugging to see a named function in the call stack. 
  
#### Example

```typescript
/* avoid */

useTask$(()=>{ 
  // some code that should run when the component is created
});

```

Give a descriptive name for the task callback function:

```typescript
/* recommended */

useTask$(function initTask(){ 
  // some code that should run when the component is created
});
```

**[Back to top](#table-of-contents)**



## Translations

If you want to translate this style guide, please feel free to submit a PR with a markdown file under `translations` folder `.md` file with the relevant locale (for example: `es-ES.md`)

## Inspirations & Credits

This style guide structure is inspired by the [Angular Style guide](https://angular.io/guide/styleguide) and the [Vue Style Guide](https://vuejs.org/style-guide/). 


## License
MIT

(Feel free to use it, attributions are appreciated 😊)