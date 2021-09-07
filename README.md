# React Native Universal Monorepo (🚧 WIP)

A React Native monorepo boilerplate supporting multiple platforms: Android, iOS, macOS, Windows, web, browser extension, Electron.

&nbsp;

<p align="center" margin-bottom="0">
  <img width="820" height="auto" src="./.github/images/all-screenshot.png">
</p>

## Overview

This monorepo uses [Yarn workspaces](https://classic.yarnpkg.com/en/docs/workspaces/) and [TypeScript](https://www.typescriptlang.org/) to support a modular React Native project.

It uses Yarn's `nohoist` to ensure the `react-native` libraries are stored within the workspace packages instead of being hosted to the top level.  
On one hand, this approach has the drawback of (potentially) keeping multiple copies of the same React Native version in different workspace packages.  
On the other hand, we get a predictable React Native setup: we don't have to deal with changing root directory references in the native code, and we can support different versions of React Native while still sharing the app's code.

> Please notice that this is not the _right_ way to do React Native monorepos. It's just an approach that I enjoy using.

## Supported platforms

- Android (React-Native 0.65)
- iOS (React-Native 0.65)
- Windows (React-Native 0.65)
- MacOS (React-Native 0.63)
- Web (React-Native 0.65)
- Web - Browser Extension (React-Native 0.65)
- Web - Electron (React-Native 0.65)

## Getting started

> 🚧 I'm working on a blog post to explain how to get to this monorepo structure from scratch.

1. Clone the repository: `git@github.com:mmazzarolo/react-native-universal-monorepo.git`
2. Run yarn install `cd react-native-universal-monorepo && yarn`

## Available commands

- `yarn android:metro`: Start the metro server for android/iOS
- `yarn android:start`: Start developing the android app
- `yarn android:studio`: Open the android app on android Studio
- `yarn ios:metro`: Start the metro server for android/iOS
- `yarn ios:start`: Start developing the iOS app
- `yarn ios:xcode`: Open the iOS app on XCode
- `yarn macos:metro`: Start the metro server for macOS
- `yarn macos:start`: Start developing the macOS app
- `yarn macos:xcode`: Open the macOS app on XCode
- `yarn web:start`: Start developing the web app
- `yarn web:build`: Create a production build of the web app
- `yarn electron:start`: Start developing the electron app
- `yarn electron:package:mac`: Package the production binary of the electron app for macOS
- `yarn electron:package:win`: Package the production binary of the electron app for windows
- `yarn electron:package:linux`: Package the production binary of the electron app for linux
- `yarn browser-ext:start`: Start developing the browser extension
- `yarn browser-ext:build`: Create a production build of the browser extension
- `yarn windows:metro`: Start the metro server for windows
- `yarn windows:start`: Start developing the windows app
- `yarn lint`: Lint each project
- `yarn lint:fix`: Lint + fix each project
- `yarn test`: Run test of each project
- `yarn typecheck`: Run the TypeScript type-checking on each project