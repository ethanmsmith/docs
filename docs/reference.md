[Home](/)  
[Athenaeum](/docs/athenaeum)

# Reference CLI
Reference CLI is a node package that allows users to create boilerplate react files akin to Angular CLI.
This is a TypeScript plugin. Though I think I will add JavaScript support in the future.

## Synopsis
```c#
NAME
    ref - creates react components and mongoose models in TypeScript

SYNTAX
    ref [-c | -m] desiredName

OPTIONS
    -c, --component  
        Creates a react component.
    -m, --model
        Creates a mongoose model.
    
```

## Examples
  `ref -c my-new-component`  
  Creates a component with the name MyNewComponent

  `ref -m my-mongoose-model`  
  Creates a mongoose model with the name MyMongooseModel
  
  **N.B.** The hyphens are removed and camel/pascal casing applied to the names of files and classes. 
  Folder names will still have hyphens.

## Description
  ref either creates a mongoose model at the path `src/models/desiredName.model.ts`  
  or creates a react component in the directory `src/components/desired-name/` with three files:
  
    - index.tsx
    - desiredName.tsx
    - desiredName.scss

## Rationale
  The component has that structure so that we can import it more cleanly. Instead of having to import a component like  
  ```TypeScript
  import MyComponent from './components/my-component/MyComponent.tsx';
  ```
  We can import like
  ```TypeScript
  import MyComponent from './components/my-component';
  ```
  
  Which looks similar to npm module imports 
  ```TypeScript
  import ThirdPartyModule from 'thirdPartyModule';
  ```

  There is also no unnecessary repetition or any file types. 
  
## Planned Work
  - [ ] Testing

