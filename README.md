# Cryptoverse - Explore the World of Cryptocurrency (TYPESCRIPT)

## Acknowledgements

The original version is availale at <https://github.com/adrianhajdin/project_cryptoverse.git>.
See also [Build and Deploy a React Cryptocurrency App and Master Redux Toolkit in One Video](https://www.youtube.com/watch?v=9DDX3US3kss)

![Cryptoverse](https://i.ibb.co/8gh5Jc8/image.png)

The TypeScript migration was done by [Volker Reichel (volker@vritb.de)](https://github.com/vritb/project_cryptoverse.git)

## Introduction

This is a code repository for the corresponding video tutorial.

In this video, we will create a cryptocurrency app in TypeScript. We're going to use React and multiple APIs powered by https://rapidapi.com.

## Using your own credentials

To run the application you need to have your own account and use your credentials. Please see original video. Link above.

## Fixing warnings before migration

1. The development console in the browser shows some warnings regarding a missing `key` attribute in lists.
   `index.jsx`, `News.jsx` and `CryptoDetails.jsx` are offending source files. To fix add the `key` attribute and assign a unique value to it. The advantage is a gain in performance in rendering the lists.


## Migration Process

1. Step Install TypeScript
   ```sh
   npm install typescript@4.4.4
   ```
1. Step Configure TypeScript
   ```sh
   touch tsconfig.json
   ```
   Copy the following snippet into `tsconfig.json`.
   ```json
{
  "compilerOptions": {
    "target": "es5",
    "jsx": "react-jsx",
    "module": "esnext",
    "moduleResolution": "node",
    "allowJs": true,
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "noImplicitAny": true,
    "skipLibCheck": true,
    "lib": [
      "dom",
      "dom.iterable",
      "esnext"
    ],
    "allowSyntheticDefaultImports": true,
    "resolveJsonModule": true,
    "isolatedModules": true,
    "noEmit": true,
    "noFallthroughCasesInSwitch": true
  },
  "include": [
    "src"
  ]
}

   ```
2. Step Rename files
   `*.jsx` -> `*.tsx` and `*.js`-> `*.ts`
