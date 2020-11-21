# NG Enterprise Conference 2020

- [NG Enterprise Conference 2020](#ng-enterprise-conference-2020)
  - [Keynote: Present and Future of Angular](#keynote-present-and-future-of-angular)
    - [Overview of Angular at Google](#overview-of-angular-at-google)
      - [Features](#features)
    - [Evergreen Nature of Angular - Misko Hevery @mhevery](#evergreen-nature-of-angular---misko-hevery-mhevery)
      - [Q4 and Beyond](#q4-and-beyond)
  - [Nx for Angular CLI Users](#nx-for-angular-cli-users)
    - [Part I: Modern Tools](#part-i-modern-tools)
      - [Nx Cloud](#nx-cloud)
  - [Sustainable Angular Architectures with Monorepos and Strategic Domain-Driven Design](#sustainable-angular-architectures-with-monorepos-and-strategic-domain-driven-design)
    - [Sustainable Architecture](#sustainable-architecture)
    - [Strategic Design](#strategic-design)
    - [DDD](#ddd)
  - [Nx - The Fun Bits](#nx---the-fun-bits)
  - [Configuring Angular Libraries with Monorepos](#configuring-angular-libraries-with-monorepos)
    - [Why Do You Need Libraries](#why-do-you-need-libraries)
    - [Create a Library](#create-a-library)
  - [Speed up! Incremental Compilation with Nx](#speed-up-incremental-compilation-with-nx)
    - [Computation Caching](#computation-caching)
  - [Angular Material and Harnesses](#angular-material-and-harnesses)
  - [Testing NgRX](#testing-ngrx)
  - [Filling the Gap in State with NgRx ComponentStore](#filling-the-gap-in-state-with-ngrx-componentstore)
  - [TypeScript for Every Part of Your Stack](#typescript-for-every-part-of-your-stack)
  - [RxJS Patterns in Angular](#rxjs-patterns-in-angular)
  - [What’s new in Angular 11, Presented by: Mark Thompson](#whats-new-in-angular-11-presented-by-mark-thompson)
  - [Micro-Frontends Decisions Framework, Presented by: Luca Mezzalira](#micro-frontends-decisions-framework-presented-by-luca-mezzalira)
    - [Decisions](#decisions)
  - [The Microfrontend Revolution: Using Webpack 5 Module Federation with Angular, Presented by: Manfred Steyer](#the-microfrontend-revolution-using-webpack-5-module-federation-with-angular-presented-by-manfred-steyer)
    - [Module Federation](#module-federation)
    - [Federated Angular](#federated-angular)
    - [Panel](#panel)
  - [Framework Inception with Micro Frontend Composition --> BULLSHIT TALK](#framework-inception-with-micro-frontend-composition----bullshit-talk)
  - [MFE Toolbox: Tips for building your micro frontend](#mfe-toolbox-tips-for-building-your-micro-frontend)
    - [Backstory](#backstory)
  - [MFE Panel](#mfe-panel)
  - [Panel: Performance](#panel-performance)
  - [Angular Performance in the Enterprise, Presented by:](#angular-performance-in-the-enterprise-presented-by)
  - [State Management Anti-Patterns](#state-management-anti-patterns)
  - [Introducing StackBlitz for Enterprise](#introducing-stackblitz-for-enterprise)
  - [Adding Real Time Collaboration to Angular Apps with Fluid](#adding-real-time-collaboration-to-angular-apps-with-fluid)
  - [Deploying Secure Angular Apps that Scale, Presented by: John Papa](#deploying-secure-angular-apps-that-scale-presented-by-john-papa)
  - [Create an unfair competitive advantage with CI/CD Pipelines](#create-an-unfair-competitive-advantage-with-cicd-pipelines)
    - [Juicy Benefits](#juicy-benefits)
  - [Panel (Friday Afternoon)](#panel-friday-afternoon)
  - [Questions](#questions)
  - [Resources](#resources)

## Keynote: Present and Future of Angular

- Jules Kremer
- Mishko

### Overview of Angular at Google

- apps users love to use
- apps developers love to build
- community where everyone feels welcome

Strengths:

- opinionated
- scalable
  - apps and teams grow; all of the applications look familiar, tool-chain is recognizable,
- ecosystem
- evergreen: enable you to keep pace with latest changes; `ng update` to get the latest feature drop

There are product groups - Angular was originally part of the Google Ads business. It was re-organized to allow the team to be more effective - building infrastructure/tools to build products at Google. 

Core Developer: make Google class development fast and easily.
Core Developer Web:

- Web Foundations: Sass, TS
- Web Frameworks: Angular, Wiz* ("Wiz Star"): ability to collaborate with teams and peers; like evolving template languages/tools; Supports all projects that use Angular at Google;

Why this Matters?

- 9/14/2016 Launch party for Angular
- 1.7x growth in # of apps since 2019 (2600+ apps at Google)
- monorepo: stable and evergreen
  - deep insights to all projects; early identification of issues;
  - chaos breaking with automation; transform projects and migrate to latest versions using `ng update`; intimate knowledge of how Angular is used getting a different perspective, practice/patterns, etc.
  - `ng update @angular/cli @angular/core` #batteries included platform

Angular Stakeholders: developers and users of the web; 

1. 1.7M Angular Developers
2. 1000's of Google Engineers

- What do users want? Github.com is the main focus for feedback and triage - feature requests; relationships with customers; GDE Feedback; Angular Surveys helps with prioritization process

#### Features

- community programs
- documentation
- infrastructure: ci, open-source repositories, and Google monorepo
- team projects: working as a team on real projects

Sweet-spot Strategy: 1. Release an Angular Roadmap that is prioritized weekly "Ng Elephant"; 2. Core Value driven; 3. Collaborative 4. "Sweet Spot" Strategy. 

### Evergreen Nature of Angular - Misko Hevery @mhevery

> https://twitter.com/mhevery?lang=en

Achievements: Ivy with version 9; size and build-time improvements; change from ViewEngine to Ivy; On over 2600 applications in Google Monorepo.

- v11: focus on technical debt; buggix, performance --> "Byelog"
  - lazy-loading modules in named outlets; router, etc.
  - forms
  - internationalization; translate templates and strings; `:alert`
    - zero-runtime overhead
    - faster loads/smaller bundles;
    - single i18n solution for template and programmatic text
    - see: Angular Localization with Ivy;
  - faster `ngcc` builds;
  - TypeScript 4.1: external source maps...
  - "Hot Module Reloading" - only laod what changed; with incremental module recompile; faster development; use `--hmr` flag with version 11
  - Ivy Language Service (preview); type-checking in templates, intellisense, etc.
  - Webpack v5 Preview
  - TSLint --> ESLint (migration path)

#### Q4 and Beyond

3.7s FCP (fist content paint) --> `ng update @angular/cli`

- render blocking resources
  - inline critical CSS
  - inline font definition
  - support:
    - CSR
    - SSR
    - App shell
    - Prerendering

Ng upgrade is evergreen.

- Webpack 5 and micro-frontends; Federation Module Loading?
- Dev tools
  - Augury --> "Angular DevTools"
    - component explorer
    - profiler (change detection, cycles, source of change detection)
- Optional NgModules
- Zoneless; limit change detection cycles; build lean apps
  - micro-optimize application by reducing change detection

Roadmap for Angular at: https://blog.angular.io/a-roadmap-for-angular-1b4fa996a771

## Nx for Angular CLI Users

- Jeff Cross @jeffbcross
- Katarina Skroumpelou; psyber.city @psybercity

By now, you’ve probably heard of Nx from Nrwl. You might know that it’s a toolkit based on top of Angular CLI, and it’s great for developing monorepos. But there’s so much more to Nx than just monorepos! In this talk, Jeff Cross and Katerina Skroumpelou will talk about everything Nx does to help you develop any Angular application better and faster.

This session looks at a solution provided by Strategic Domain-Driven Design. Using an Angular-based case study, we investigate the idea of the ubiquitous language and the bounded context, sub-domains, and context mapping. Building on this, you will learn how to implement these ideas for Angular using a monorepo. We also discuss approaches for reducing coupling between the specific parts of our monorepo.

By the end, you will have a technical solution and appropriate methodology to build sustainable Angular solutions.

### Part I: Modern Tools

- ESLint
  - part of the selection process
- Cypress
  - new apps get e2e tests by default; headless and heeded modes with screenshots and videos
  - use `--watch` mode for headless
  - code completion
- Jest
  - default unit test runner for frontend apps; fast to write/execute tests
    - fast and fun
  - well-maintained project
- Storybook
  - develop components in isolation; develop and test components; shared libraries
  - Nx configures Storybook configuration with Cypress integration
    - build, serve, and watch
    - `nx g @nrwl/angular:storybook <name>`
- Prettier
  - sets up Prettier
  - formats only changed files

> `npx create-nx-workspace <name>` <options>

> see: https://github.com/nrwl/nx-examples

#### Nx Cloud

- developer --> Nx Cloud <--> CI (affected, parallel, incremental cache)
  - up to 10x build performance
  - use Nx Console plug-in

> see: https://nx.dev/modern-angular

## Sustainable Angular Architectures with Monorepos and Strategic Domain-Driven Design

> Start as lean as possible. Refactor when you need to with Nx Workspace. Monorepo + micro-frontend can/will work together. There is more overhead of having separate workspace/projects to manage deployable artifacts - an application or library can be deployed independently from a monorepo easily (Jeff Cross), using a single-version dependency.

- Manfred Steyer
  - https://www.angulararchitects.io
  - https://www.angulararchitects.io/workshops

Monorepos allow huge enterprise applications to be subdivided into small and maintainable libraries. However, this is only one side of the coin: We need first to define criteria for slicing our application into individual parts and establish rules for communication between them.

This session looks at a solution provided by Strategic Domain-Driven Design. Using an Angular-based case study, we investigate the idea of the ubiquitous language and the bounded context, sub-domains, and context mapping. Building on this, you will learn how to implement these ideas for Angular using a monorepo. We also discuss approaches for reducing coupling between the specific parts of our monorepo.

By the end, you will have a technical solution and appropriate methodology to build sustainable Angular solutions.

- difficult to change things in chaos
  - use ideas from DDD; bridge the gap between requirements and design
- Strategic Design
  - decomposing a system; larger into smaller parts
- Tactical Design
  - patterns and practices

### Sustainable Architecture

Sustainable: invest up-front to have SW that lasts
Ideas: use the ideas and tools to get where you need to be

### Strategic Design

> Do not write a monolith application?
> book: https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215
> book: [Angular Enterprise](https://leanpub.com/enterprise-angular) - free on website above.

- Create smaller sub-domains to organize your domains/code
- isolate the domains (abstraction) - decoupled
- define the dependencies between each of the domains
  - how they communicate
  - direct and full access?
- expose only selected APIs
  - backwards compatible
  - open-/Host-Service (DDD) --> API

> Shared Kernal: is a bad idea; shared libraries between all domain libraries

Categories of Libraries (types) --> basically code organization

- feature library: has a specific use-case; has components
- utility: with dumb components
- domain: domain logic/BL
- utility layer: security, logging, notifications, etc.

Horizontal and vertical management of application concerns. Use the [tag] feature to define dependencies for control access restriction.

- instead of `shared kernal` use an API to expose only what needs to accessed by other libraries (access restrictions)
- avoid highly-coupled situations
- NX [tag] --> `nx.json`
  - define categories
  - use `tslint.json` or `eslint.json` files to configure
  - provides notifications/messages in IDE during attempted imports
  - checked by using *lint* errors - if the access restrictions is violated
- fine-grained libraries better maintenance
- use `library` projects instead of `ngModule` in applications

> Demo: empty Nx workspace: `ng add @angular-architects/add`
> Github: https://github.com/search?q=%40angular-architects&ref=opensearch
>
> - app: https://github.com/angular-architects/ddd-demo

### DDD

If there are some/any pain points, start using DDD concepts the code organization strategies using Nx libraries.

- 80/20: copy/move current projects to new Nx Worksapce
- 20%: refactor to optimize

## Nx - The Fun Bits

> Use Nx to be more productive - use the tooling to be more effective and efficient.

Nx has some very cool things that make it fun to use to create and manage your frontend and fullstack applications. In this lightening talk, we will go over some of the things that makes Nx a joy. See you there.

Yvonne Allen is currently a Developer Advocate at Vonage, maintaining the Vonage Java SDK. Yvonne has previously worked as a Angular Fullstack Developer for companies such as Rangle.io and NCR. She is a newcomer to speaking at conferences with her most recent being IonicConf and NgConf Hardwired. Yvonne is a co-organizer for GDG Atlanta, a member of Women Who Code, and Women Techmakers. She has a passion for advising and mentoring new developers and is an open source contributor.

- Extensible dev tools
- Join office hours on YouTube.com and/or Twitch

> https://go.nrwl.io/nx-office-hours
> YouTube.com: https://www.youtube.com/watch?v=ChQsqGheQzc

## Configuring Angular Libraries with Monorepos

> You can start with moving related/unrelated apps to a monorepo; then move towards library projects to support the application, features, and other cross-cutting concerns. Organize your code - multiple applications from different teams provides a lot of efficiency, code reuse, best practice, etc.

- Nishu Goel

Building features and writing logics with a reusability mindset is a rewarding experience in the current era of a componentized web. This session will take you through a journey of building your amazing features as Angular libraries and managing those complex libraries/projects effectively inside a single workspace.

### Why Do You Need Libraries

- Reusability: allows you to share and reuse a feature with other projects (application and/or library project types)
  - may contain components, modules
  - shared code
  - reuse of functionality
  - dedicated code for a feature
    - build in advance for reuse
    - code organization

> "smallest set of logically connected code"

### Create a Library

- An Angular library should be:

  - platform independent (work with )
  - bundled and dsitributed
  - use APF (ng package format); typed, entry points, etc.
    - inline all templates and styles
    - compile with `ngc` compiler
  - use `ng-packagr`

> Monorepo: single location/workspace for apps and libs. shared code and feature code; common 3rd-party dependencies; common configurations, practices and patterns. Need to understand the meaning, benefits, etc.; learn and understand Git effectively within a monorepo.

- create
- consume/use without build/publish

> see: Nishu Goel:
>
> - https://medium.com/angular-in-depth/step-by-step-guide-to-creating-your-first-library-in-angular-6827276bfc9f
> - Creating a library: https://github.com/NishuGoel/ngSLDemo
> - Consuming the library: https://github.com/NishuGoel/consuming-angular-lib

## Speed up! Incremental Compilation with Nx

> Do not enter a monorepo naively - all users need to know/understand monorepo; with Git. Team and management will need to support the monorepo with: collaboration, communication, sharing; align your SDLC or other processes to align with the monorepo; this includes the business processes to create micro-projects that support the monorepo.

- Juri Strumpflohner
  - [more info](https://www.google.com/search?q=Juri+Strumpflohner&oq=Juri+Strumpflohner&aqs=chrome..69i57j0i22i30l3.1053j0j7&sourceid=chrome&ie=UTF-8)
  - twitter: @juristr

> About: Juri Strumpflohner lives in the very northern part of Italy and is currently working as a JavaScript Architect and Engineering Manager at Nrwl, where he consults for some of the world’s biggest companies around the globe. Juri is very involved in the community. He’s a Google Developer Expert in Web Technologies & Angular, speaks at international conferences, teaches on Egghead.io, or writes articles on https://juri.dev. He’s also a core member of Nx.

At Nrwl we work with some of the world’s biggest companies. By working alongside their teams, we directly experience the problems and pain points they face on a daily basis, especially when it comes to scaling products and code bases across such large enterprises. These lessons directly influence how we build Nx. We understand the importance of proper DX and how much time and money it can save businesses. Speed is one such important characteristic. The fewer time developers have to wait for their CI pipeline to finish, or their app to recompile, the less they get distracted and hence can be more focused and productive. We recently introduced Nx’s computation caching, which together with Nx Cloud addresses precisely that problem. In this talk, we’re exploring how computation caching enables us to go to the next level: implementing incremental compilation in Nx.

- Nx Building Blocks
  - apps and libs
  - split SPA to multiple applications
    - apps
    - feature libraries
  - NestJS
  - nodeJS
  - other Tech
    - React

Isolated build, test, and lint - scale and performance.

- linear; total time of sequential builds
- distributed CI pipeline builds

Use: `nx affected:test --parallel`. You can use local or cloud-based caching with Nx.

```ts
nx build app
nx serve app
nx g @nrwl/angular:lib mylib --buildable #different from --publishable

# incremental build concepts
nx build app --with-deps #builds the dep-graph (or uses cached); lowest level up the tree;
```

> see: https://github.com/nrwl/nx-incremental-large-repo

### Computation Caching

Checks to determine if the resources/artifacts already exist in Cache - from a previous executed run/output of the CLI.

## Angular Material and Harnesses

- Emma Twersky :: @twerske

The Angular roadmap announced the expansion of Material component harnesses and best practices, but what does this mean for developers? Soon, there will be a harness available for every Material component! In this talk, we will dive into the motivation behind Material’s component harnesses and the benefits they bring developers. We’ll also cover how to migrate to and use Material component harnesses, and how this fits into the upcoming integration of MDC Web into Angular Material.

Benefits:

- robust testing; less fixes when internal components change; 
- async behaviors
- accessibility
- easy to read and understand

All MDC have their own test harnesses - all in version 11.

- overriding styles and css
- screenshot tests
- non-supported test environment

> Start migrating to Material harnesses.

## Testing NgRX

- Cecelia Martinez :: @ceceliacreates

Interested in adding NgRx store validation to your UI or end-to-end tests? With Cypress, you can access your NgRx store in the browser to make assertions and even dispatch actions for testing. Learn how to better validate the behavior of your NgRx store when responding to real input in a browser.

Test Application: [thisdot-ngrx-testing](https://github.com/ceceliacreates/thisdot-ngrx-testing)

- forked from: https://github.com/frederikprijck/thisdot-ngrx-testing

## Filling the Gap in State with NgRx ComponentStore

- Alex Okrushko

Synchronizing state within the app and backends is one of the most complicated parts of writing web applications. There are a number of solutions for global/app-wide state management, however, a more localized state was left behind. Let me introduce the latest addition to the NgRx family of libraries – @ngrx/component-store – a standalone library for managing local/component state, which intends to be a replacement of “Service with a Subject”.
What’s the State? Why do we need to manage it? What problems are we trying to solve? These are the questions they we will during the talk.

- Service with a Subject approach
  - make a call/function that returns `void`; it triggers events to push data to an Observable stream that exists
  - click `add` race-condition; use effects to handle that;
  - see: `@ngrx/component-store`
    - read
    - write
    - handle side-effects

> "Think of state as a first-class citizen." - Alex Okrushko

## TypeScript for Every Part of Your Stack

- Ryan Chenkie :: @ryanchenkie

The confidence we get from TypeScript in our Angular apps is great but what about the other parts of our stack? While it’s common to use TypeScript in an Angular app, it’s less common to use it in a Node backend. It’s especially less common to see database access be type-safe.
In this talk, we’ll look at how your team can be more productive by using the same types for your Angular app, TypeScript Node server, and also database access with Prisma. We’ll show how to do all of this in an Nx monorepo.

> Tool: Prisma, `@prisma/client`, `@prisma` package.

## RxJS Patterns in Angular

Deborah Kurata

> Deborah Kurata is a software developer, speaker and Pluralsight author with a focus on C# and Angular. For her work in support of software development and software developers, she has been recognized with the Microsoft Most Valuable Professional (MVP) award and is a Google Developer Expert (GDE). Follow her on twitter: @deborahkurata

Following common RxJS patterns can save you time, and improve the quality and simplify the maintenance of your Angular code. This session walks through several common coding scenarios and useful RxJS patterns to implement those scenarios.

https://stream.mux.com/8vyUvSdeVCxBGWc02ebhtIRc4nLBlLJJuEvzyJI800JJ8.m3u8

## What’s new in Angular 11, Presented by: Mark Thompson

Mark Thompson :: @marktechson

- "Apps users love to use"
- "Apps developers love to build."
- "Community where everyone feels welcome."

Angular version 11 is here! This new release comes with great platform improvements and important changes. Together we’ll dive into some of the highlights and why you should update today!

- 2-4x ngcc builds
- supports TS v4
- Experimental support for Webpack v5
  - module federation in the ClI
  - resolutions: {"webpack": "5.0.0"}
- HMR (hot module replacement)
  - CLI updated to use HMR: use `ng serve --hrm` # async reload without a full refresh
- ESLint (deprecated); use Angular ESLint for now.
- Better CLI output and logging (reporting);
  - easier to read
- API Deprecations
  - see: angular.io to see which APIs were removed

```ts
ng update @angular/cli @angular/core
```

## Micro-Frontends Decisions Framework, Presented by: Luca Mezzalira

Micro-frontends are a new architectural trend in the development of frontend applications. This architectural style can provide several benefits to your projects and organization, offering a level of decoupling never seen before in single-page applications or universal architectures. Based on his work at DAZN, Luca Mezzalira explains how to implement micro-frontends using the Micro-Frontends Decisions Framework, 4 pillars will guide the design of any micro-frontends project.

- "...a technical representation of a business subdomain; independent implementations"
- "avoid sharing logic with other sub-domains..."

Principles

- model around business domain
- decentralization: allows a team to own the micro-app/frontend
- culture of automation
  - iterate on pipelines/CI
  - validate and improve feedback validation
- allow to deploy independently
  - requires analysis --> is it really independent?
- Hide implementation details
- Isolate failures

> micro-frontends DECISIONS FRAMEWORK
> USE TO DETERMINE IF IT RIGHT...

1. DEFINE

- horizontal or vertical splts of micro-frontends
  - horizontal:
    - 1. upfront investment
    - 2. teams structure: consider business process, flows, and how teams work together/collaborate
    - 3. testing challenges
    - 4. scalability challenges: caching?
    - 5. dependency management: different versions of Angular in the same view? How to manage? Module Federation (deals with this).
  - vertical:
    - 1. traditional dev
    - 2. embrace JS ecosystem
    - 3. dynamic rendering for SEO; serve an optimized version of your content (see Google online for more techniques)

2. COMPOSE

- origin --> cdn --> client (loads different micro-frontend) when requesting a different route
- origin --> cdn (only)
- compose at application server-layer (SSR); caching data/content on S3 (partially or fully).

1. ROUTE

- a. ??
- b. URL changes use CDN to change content
- c. use application server

3. COMMUNICATE

- changing states and communicating with other micro-frontends
  - use a de-coupled mechanism (pub/sub)
  - avoid strict coupling
- use querystrings with (id)
- use session storage, local storage.

### Decisions

- Observability
- Automation
- Design system
- dep management
- performance

- [O'Reilly Building Micro-Frontends by Luca Mezzalira](https://medium.com/@lucamezzalira/building-micro-frontends-the-book-a2b531d0279a)
- https://www.oreilly.com/library/view/building-micro-frontends/9781492082989/
- https://www.buildingmicrofrontends.com

https://docs.google.com/presentation/d/1EWcJlSxvzwwjGNH7UrXmGHS7ofZPv_OVxzKHo-A4Zzw/edit?usp=drivesdk

## The Microfrontend Revolution: Using Webpack 5 Module Federation with Angular, Presented by: Manfred Steyer

The implementation of micro frontends has so far been anything but easy. Since common frameworks and build tools didn’t even know this idea, you had to dig into the tricks bag.
Module Federation offered by Webpack 5 initiates a crucial change of direction here. It allows you to load separately compiled applications at runtime and to share libraries between them.

In this session, you will learn how to use this mechanism to create micro frontends with Angular. Besides the default scenarios, we also look into dynamic Module Federation and into sharing libraries.

At the end of the session, you know how to use Module Federation in your projects and the consequences.

> Intro: Davinci helicopter design really works.

### Module Federation

- how to load separately compiled code/app for a micro-frontend
  - use dynamic import? not supported by Webpack
  - most bundling solutions assume all lazy-parts are known at compile time
    - not supported by the Angular CLI...
    - all things are compiled together --> chunks of JS bundles
- Webpack 5
  - host (shell): the application ("mfe1")
    - `import ...c`
  - remote (micro-frontend) "c"
    - expose files in webpack config: `exposes: { `./Cmp: '.my.component}`
    - remoteEntry.js shared/exposed
      - Webpack emits an entry point for the Micro-Frontend (MF)
      - load using a `<script>` tag
    - shared: ["@angular/.."] libraries (or other libraries) with host and remote
  - dynamic module federation

> do not make your software architecture to be an incredible machine

### Federated Angular

- Angular CLI uses WebPack
  - con: shields the use webpack...
- consider using a custom builder
  - adds MFC (module federation configuration)
  
> see: @angular-architects/module-federation

- generates mfc
- installs
- etc...

```ts
ng add @angular-architects/module-federation
# adjust config
# serve
```

More info: https://www.google.com/search?q=manfred+stayer+module+federation+with+angular&oq=manfred+stayer+module+federation+with+angular&aqs=chrome..69i57.12272j0j4&sourceid=chrome&ie=UTF-8

- [Module Federation with Angular](https://github.com/manfredsteyer/module-federation-with-angular)
- [The micro-frontend revolution part 2](https://www.angulararchitects.io/aktuelles/the-microfrontend-revolution-part-2-module-federation-with-angular/)

### Panel

- Web Components vs MicroFrontend with MF
  - WC hidden by shadow DOM
  - MF apps are found by SEO (no iframe)
- How do MF communicate between each other?
  - use Decision Framework
  - client-side communication (share a service)
    - with BehaviorSubject that implements messaging for the listeners (micro-apps)
    - when you load multiple MFE in same view; need to buffer events
    - the application shell needs to allow a replay of the messages to allow the MFE to start in the right state and/or catch up to the state
- Does that communication couple the MFEs?
  - No, allow broadcasting but do not require a response back from the MFE back to the BehaviorSubject/Service
  - Communication is an issue - isolated MFE vs. MFE with communication with other MfE --> creates some dependencies; there is a trade-off based on the context of the application.
  - Compare to MS on BE; use queues or pub/sub (stream); leverage the same concepts; choreography, creating and sharing events in a system that allows some part of the view to react (if they want to - not required); without requiring deps on load of the MFE (with state)
    - queues
    - array buffers
    - reactive streams
- How likely is the NgRX Store the service??
  - Not, do not want the coupling.
  - Share that something changed and allow a reaction to the event (but not required by other MFEs).
  - Use a decoupling system/mechanism to share information/data/state - but do not require dependency from the MFEs; be mindful on what you want to share - keep it flexible for delivery and future
  - shared state requires a different architecture to keep the MFEs decoupled
- How do I share reusable components with other MFEs? or sharing `widgets`
  - use `web components` especially when there are different frameworks involved (e.g., Angular and React or Vue).
  - sharing `widgets` may create highly-coupled MFEs.
    - make sure the `widgets` are not domain-specific
- How do I prevent duplication (i.e., components/widgets, x-concerns) across MFEs?
  - ex: header/footer sharing; change infrequently
  - centralizing a `header` vs having a copy of the `header` for each workspace/application
  - create a shared component hosted on npm (video player); with managed semantic versioning;
    - check versions of deps during build process?? (Fitness)
  - MFE is a business domain; with a specific objective (not a code duplication); uses different data for the implementation
- How to do authentication on a page with MFEs?
  - defer to the app-shell; share your Interceptors in shared package to allow other MFEs to check for authorization
  - each MFE utilize the token using Interceptors
  - consider storing the token in `local storage` - based on subdomain?? allows access from other MFEs;
    - preference: use a centralized mechanism to handle the communication
  - make sure the MFE can be tested in isolation without requiring the shell to pass the token
- How do I plugin other MFEs into a shell dashboard - to display data from other `widget`?
  - ex: NewRelic views are dashboards; initial and extended views using MFEs as `widgets` with a button to access the MFE target
  - each widget is domain-specific where a different team manages the `shell` to compose the views using the MFEs;
    - a team may create an MFE that breaks the app...?
    - be careful when using more than 1 MFE on the main view
    - OK to develop the dashboard as its own DOMAIN - as a MFE
- What are the most beneficial parts of Federated Modules?
  - Tobias Koppers: It removes technical restrictions/limitations common to MFEs.

## Framework Inception with Micro Frontend Composition --> BULLSHIT TALK

Presented by: Lukas Ruebbelke

Micro frontends solve complex developer problems, but more importantly, they accelerate innovation by giving organizations an incredible advantage through composition at the architecture layer. The future is a world where framework supremacy is a discussion relegated to the sidelines, and achieving business outcomes through composition will become the focus. In this talk, we will see what this looks like in a practical demo and how you can start to apply these ideas to your development efforts.

Organizational Complexity

Module Discovery #ledger; query the ledger to see if other modules are available.

## MFE Toolbox: Tips for building your micro frontend

Presented by: Derrick Mitra (Adesa|Openlane)

A closer look inside our Micro Frontend toolbox. I will discuss our approach to our application shell, building our MFEs in Angular / Vue, and reusable web components in Stencil. Additionally, I will discuss how we have approached shared aspects of our application and performance.

### Backstory

- (3) different platforms; legacy, whitelabel, modernization projects, distributed teams
- Scalability Issues
  - move from a monolith
- Goals
  - see image;
  - use `manifest.json` - use Webpack Manifest plugin (PWA in Ng creates a manifest.json file)
  - use a selector in the index to target the MFE
  - data sharing
    - session storage
    - local storage
- Styles
  - mangaged by the shell

## MFE Panel

- Should one team own the shell application?
  - Yes, however have a member on that team as a member of the MFE team also.
  - Or, have a community of practice to allow different developers to contribute and manage
    - shares the knowledge
- MFE and monorepos together - use MFE without a monorepo?
  - production v consumption;
  - monorepo good for production - low-impedance workflows;
    - allows complexities to be abstracted
  - consumption: as MFE is a `runtime/production` thing.
- Can we really get 4x speed improvement with `ngcc`
- Why switch from Angular Elements to "Stencil"?
  - compiles to native JS
  - compatibility with legacy apps/platform (e.g., jQuery, MooTools, etc.)
- How do MFE work with Routing on the shell?
  - there is just lazy-loading routes --> points to a different origin
    - looks the same with MF
    - if not MF, requires a meta-router mechanism
- Can we support multiple UI frameworks using MF?
  - shell:React with MFE:Angular or any other framework as the MFE
  - when you need `interop`/communication between the MFEs and shell
    - you can put multiple frameworks on a shell - you will have trade-offs
- How can an organization their MFEs do not become coupled over time?
  - discipline as developer practice
  - [Fitnesse functions](https://www.broadcom.com/sw-tech-blogs/mainframe/ci-cd-pipelines-and-architecture-fitness-functions-for-mainframe-platforms-and-beyond-software-scale); make sure that they do not communicate together; guard/gate at the CI level
    - see book: "Revolutionary Architecture"
  - create Fitness function via Lighthouse
    - static analysis/cyclomatic-dependencies
  - create feedback loops to get feedback --> invest time on the CI part
  - use-case driven; a share-nothing architecture
    - use Nx access restrictions via configuration --> loose-coupling
  - [Pareto Principle](https://en.wikipedia.org/wiki/Pareto_principle)
- use `e-tags` to cache-bust the MFE (Native Js)
  - with MF - it is supported by the `hash` name in the bundle
- Do I need MF with MFE if I am using Nx with feature/libraries that lazy-load - all applications are in the same workspace? Are there future benefits to using MF/MFE now?
  - if you need to deploy separately, use MF/MFE;
  - use Nx when you can deploy as a monolith
- If you have one or more MFEs deployed - how do you limit the access to the MFE without going through the [Shell] application?
  - cannot be prevented; access to MFE;
  - the S/W interacts with the BE; should require tokens or HTTP-based token to interact with the BE or APIs.
    - the `app` needs to be authenticatedd with the BE
  - setup CORS with BE domain server; specifiy which domains can access APIs;
    - block other requests
    - MFE should refresh/validate the token to make sure it is `authenticated` as a user/app
  - do a validation on the `token` to protect the MFE application
    - maybe a shared `HttpInterceptor` that can authenticate the app (`bearer token)`
    - refresh on a tight-schedule to make sure all users/apps are authenticated
- Webpack.config files - will this be supported by Angular as part of the eco-system? 
  - angular.json? implementation; currently no plans for integration;
  - no decision from ng team - use community tools to support.
  - use plug-in from Manfred Stayer

## Panel: Performance

- Identifying memory leaks
  - use dev tools; Pupeteer, Benchpress
- Virtual Scrolling
  - consider usingn @angular/material CDK

## Angular Performance in the Enterprise, Presented by: 

Minko Gechev :: @mgechev

In this presentation, we’re going to focus on the runtime performance of Angular applications. First, we’ll learn how to profile an app using Chrome DevTools. After that, we’ll identify different patterns looking into the profiler’s output. For each one of them, we’ll discuss strategies for reducing the runtime performance and their consequence.

- disable mangling
- use incognito browser window
  - record performance

```ts
npm i -g serve
```

1. change detection
   1. parent --> children
   2. less components
2. virtual scrolling
3. pagination
4. render on demand (IntersectionObserver)

## State Management Anti-Patterns

Presented by: Lara Newsom :: [@LaraNerdsom](https://vi.to/attendee/hubs/enterpriseng#/participants/lara_newsom)

> Lara is a software engineer consultant working at Source Allies in Urbandale, Iowa. She started her career in web design and made the transition to software development using online resources and on the job learning. Lara is passionate about sharing her experience of learning to code and helping others find resources to help them reach their own goals. In addition to learning, writing, and teaching code, Lara enjoys trail running and fostering homeless kittens, but not at the same time.

Whether we realize it or not, we are already managing state in all of our applications. How we manage that state can dramatically improve development times and application performance. In this talk we’ll cover some of the most common state management anti-patterns and discuss solutions to get out of them.

> Anti-pattern: a common solution to a problem that is a bad idea. May introduce bugs, issues, or difficulty understanding the code. Lack of understanding how things work.

- Only One Single Source of Truth
  - Direct Entity Duplication
    - any changes to a list or item in a list needs to be managed in a single place
  - Implicit State Duplication
- FrankenState
  - an application `client state --> shared state <-- managed state`
  - state management --> requires planning;
  - be thoughtful about boundaries, on how you manage state
- Observables/RxJS
  - failing to unsubscribe --> memory leaks
  - use a sub variable and unsubscribe in `ngOnDestroy`
  - use `takeUntil(this.unsubscribe)`
  - use `async` pipe subscribes/unsubscribe --> preferred
  - use pipe operators to eliminate race conditions
- Stateful Streams
  - do not use external sourced variables
- Redux Anti-Pattenr: Sharing Actions
  - do not share actions;
  - create a separate action for the consumer of the action
  - 'on' --> set of `action`; actions trigger effects (reducer);
- do not use broad selectors - use composed selectors with discreet data
- Overly complicated Effects

> More at: https://www.sourceallies.com/2020/11/state-management-anti-patterns/

## Introducing StackBlitz for Enterprise

Presented by: Eric Simons

All the power of StackBlitz, now behind your firewall. Learn how to supercharge your company’s productivity with the instant online IDE used by the official Angular documentation and many other Fortune 50 companies.

- Online IDE with Stackblitz
  - instant online IDE/VisualStudio
  - enhanced collabortion; share and reuse;
  - share with designers;
  - automated dev environments using stable templates
    - good for PR, POC, etc.
  - centralized access controls and security
    - save code in cloud; not on a laptop;
- IDE Thin Client --> no internet connection?
- Thick client, slim server
  - Zero footprint
  - web assembly
  - boots in milliseconds
  - secure sandbox
  - works offline as a PWA

Use cases:

- Angular Documentation
- use Stackblitz API to create instances for a documentation item.
- minimal reproduction on Stackblitz for a `bug report`
  - accelerates the communication flow with teams and developers
- Stackblitz can run on-premise
  - supports custom SSO
  - private npm registries
  - integration with: Github, Gitlab, etc.

## Adding Real Time Collaboration to Angular Apps with Fluid

Presented by: Dan Wahlin

As more and more of us work remotely the need for real time collaboration within applications is becoming increasingly important. How do you add a robust set of real time collaboration features into your app though? In this session, Dan Wahlin will discuss how to make that happen with a new Open Source project called “Fluid”. You’ll learn the “what, why, and how’s” of Fluid, what Fluid offers over raw web sockets, and how you can get started using Fluid in your applications.

- How do you collaborate - real time?
- Collaboration First Process
  - ask questions...it is called design;
  - collaborate at the string-level (i.e., Google Docs)
- [FluidFramework.com](https://fluidframework.com)
  - uses WebSockets; provides a way to move data structures, sync/merge data
  - DDS Distributed Data Structure
    - shared ____ that send `Op` (operation);
    - a `Dataobject` with multiple `DDS` items that work with a View
    - uses `Ops` between `Fluid Service` and the `Storage`
    - `views` are updated on separate clients of the data service

> https://podcasts.apple.com/us/podcast/fluid-framework-opensource-with-dan-wahlin/id886295635?i=1000490861592
> https://www.m365devpodcast.com/e/fluid-framework-opensource-with-dan-wahlin/

- [Fluid Framework Angular Examples Repository](https://github.com/DanWahlin/FluidAngular)

## Deploying Secure Angular Apps that Scale, Presented by: John Papa

You’ve built an app and you want it to scale. Do you want CI/CD, custom domains, SSL certificates, APIs, global scale of your static assets, authentication, and authorization? And whether your company uses Svelte, Vue, React, Angular or something else entirely, you’ll learn how to build a static web app on Azure and go from GitHub repo to global scale.
Here are some of the topics you’ll learn about:
🔒 SSL & Custom domains 🔑 Authentication/Authorization ⚙️ Automated build/deploy w/ Github Actions 👓 Preview URLs for staging 🌐 Global distribution ⚡️ APIs powered by Azure Functions

- build, host
- auth
- API
  - create endpoints (AWS)
- Github --> action to build and publish (CI)

learn: https://aka.ms/ng20-learn
github: https://github.com/johnpapa/hello-worlds
docs: https://aka.ms/ng20-docs

## Create an unfair competitive advantage with CI/CD Pipelines

Presented by: Alice Paquette :: @aliceindev

> Alice is a Senior Enterprise Software Engineer at Briebug. A ravenous learner, she seeks out new puzzles and challenges as if hunting for treasure, relentless and chock full of enthusiasm. Her latest forays include diving into the crazy world of DevOps, cooking the perfect curry, and learning Unity in an attempt to play Dungeons and Dragons virtually. Of course, good old regulars such as music, pizza, and World of Warcraft remain staples which never fail to disappoint.

Growing a company is painful. At the enterprise level, the hundreds of processes involved in getting code from a developer to your customers can often look like an incomprehensible tangle of spaghetti, making every new release a series of headaches matching the length and complexity of your delivery pipeline.
Fear not — Continuous Integration and Continuous Delivery (CI/CD) are here to help. In this talk, you will learn what those four innocuous words mean, and how they will both simplify AND turbocharge your pipeline, all the while reinforcing both your team’s and your customers’ confidence in the product you deliver.

- "Do you hate releases?" - "Playing catch up...?"
- everyone is stressed...
- CI/CD
  - structure your delivery pipeline --> from developer (business) to customer
    - version control
- Continuous Integration
  - merging code often, multiple times each day
  - should go to a main shared location; a dedicated branch (a long-lived branch)
    - trunk, main, etc --> `trunked-based` development??
- Continuous Delivery
  - trunk|main|master is always releasable
  - every merge to trunk has the potential to be `deployed`
- Automation
  - essential for integration; confidence;
  - assertain that trunk is always releasable
- MVP
  - use a primary branch
  - integration code often
  - use automated tests
- Feature Toggles
  - advanced subject --> further research required.

### Juicy Benefits

- confidence in product (more checkings)
- increased collaboration
- increased code quality (no more long-running feature branches)
- more frequent/releases
- immediate ROI
- ...
  - happy developers
  - sad competitors
  - happy dog|family

## Panel (Friday Afternoon)

- Does Stackblitz integrate with Azure DevOps - code repository?
  - not sured; works with Git processes/flows
- What are pure pipes?
  - Minko: same result with same arguments; reuses result if same arguments
- Can Fluid integrate with NgRx, GraphQL, MFE/FM?
  - YES
- Should you create your own custom CI/CD pipelines?
  - yes, but keep it simple using the tools from Github|Gitlab, etc.
  - pipelines as a service
- Are the capabilities demonstrated available in Github also?
  - It is coming...?
- Are there tools or linting rules to check for TS anti-patterns?
  - Hmmm, not sure.
- Is it possible to set scope in Fluid (e.g., chat rooms)?
  - Yes, use quaroms?
  - fluid is a platform for syncing data; doesn't do what Firebase does
- What are the limitations of NodeJS with StackBlitz?
  - running binaries that are not available as Web Assembly modules
  - JamStack: hard to find things that do not work properly
  - eric@stackblitz.com or enterprise@stackblitz.com

## Questions

1. Does MFE eliminate version differences?

## Resources

- https://oasisdigital.com/angular

Secret Words:

- Auth0 - Passwordless
- Grape City - Wijmo 2020
- Hero Dev - Heroes
- Infragistics - Dock Manager
- Kendo UI - Katana
- Nrwl - Pigtusk
- Oasis digital - results
- Ranglio.io - Augury
- StackBlitz - JACOB
- Thinkster - Grok
- XLTS - XLTS

To get the secret word, visit https://www.infragistics.com/products/ignite-ui-angular 
And look for the Exclusive Feature of Ignite UI for Angular! Feel free to ask to confirm that you have it right!

FREE Angular course: https://thinkster.io/topics/fundamentals-of-angular

50% OFF Thinkster Pro: https://thinkster.io/pro/yearly/enterpriseng

Secret Word: https://docs.google.com/forms/d/e/1FAIpQLSfCiDOhJnLsKeLlRRRD7vXQfQat5f7dLOtt9AV6Bpbx7eLCqA/viewform?usp=sf_link

[Tech Course Creator](https://techcoursecreator.thinkster.io/p/thinkster-io-authoring-course/?product_id=1798206&coupon_code=300OFF)

Auth0 Pattern: https://auth0.com/docs/auth0-email-services/send-email-invitations-for-application-signup

[Solving Common RxJS Scenarios in Angular with Deborah Kurata on Real Talk Javascript #91](https://johnpapa.net/solving-common-rxjs-scenarios-in-angular-with-deborah-kurata-on-real/)

- Podcast version: https://webrush.simplecast.com/episodes/episode-91-solving-common-rxjs-scenarios-in-angular-with-deborah-kurata

- [The Angular Show Podcast](https://open.spotify.com/episode/6QItH9k192HgEySI8PWIPp)
- [ng.show](https://ng.show) or [The Angular Show](https://www.spreaker.com/show/angular-show)
- [Angular Discord](https://discord.com/invite/angular)
- [Getting Started in Developer Relations (eBook)](https://learn.samjulien.com/getting-started-in-developer-relations)
- [samj.im/path-to-angular](https://samj.im/path-to-angular)
- [Angular Enterprise](https://www.angulararchitects.io/en/book/)

- 20 minute rule, then reach-out to your mentor.
- read the documentation (RTFM)
- "Lean in on TypeScript; be typed...it will show you the way" - Frosty
- Code Quality Enforcement in CI
  - GitHooks: unit test failures
  - code coverage threshold
  - TSLint rules, Codelyzer (deprecating?), Spelling checks
  - Cypress e2e - code coverage thresholds
  - Prettier --> format on Save!
