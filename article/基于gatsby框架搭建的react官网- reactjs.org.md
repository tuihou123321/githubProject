# 基于gatsby框架搭建的react官网- reactjs.org



## 项目说明 

基于react技术实现的一个react官方文档网站，主要介绍react语法，使用技巧；

**项目地址**：https://github.com/reactjs/reactjs.org

**在线演示**: https://reactjs.org/



### 技术栈

- react+react-router     //react全家桶
- gatsby    // react静态网站生产器         
- yaml 语言    //使用yml文件来写配置文件，代替json



### 启动
```javascript

```
访问： http://localhost:8000



### 目录结构

```$xslt

│  CODE_OF_CONDUCT.md
│  CONTRIBUTING.md
│  crowdin.yaml
│  gatsby-browser.js
│  gatsby-config.js
│  gatsby-node.js
│  LICENSE-DOCS.md
│  package.json
│  README.md
│
├─.cache
│  │  .eslintrc.json
│  │  api-runner-browser-plugins.js
│  │  api-runner-browser.js
│  │  api-runner-ssr.js
│  │  api-ssr-docs.js
│  │  app.js
│  │  async-requires.js
│  │  babelState.json
│  │  create-react-context.js
│  │  default-html.js
│  │  dev-404-page.js
│  │  dev-loader.js
│  │  develop-static-entry.js
│  │  emitter.js
│  │  ensure-resources.js
│  │  error-overlay-handler.js
│  │  find-path.js
│  │  gatsby-browser-entry.js
│  │  json-store.js
│  │  loader.js
│  │  match-paths.json
│  │  navigation.js
│  │  normalize-page-path.js
│  │  page-renderer.js
│  │  pages.json
│  │  prefetch.js
│  │  production-app.js
│  │  public-page-renderer-dev.js
│  │  public-page-renderer-prod.js
│  │  public-page-renderer.js
│  │  react-lifecycles-compat.js
│  │  redirects.json
│  │  register-service-worker.js
│  │  root.js
│  │  socketIo.js
│  │  static-entry.js
│  │  strip-prefix.js
│  │  sync-requires.js
│  │  test-require-error.js
│  │
│  ├─caches
│  │  ├─default-site-plugin
│  │  ├─dev-404-page
│  │  ├─gatsby-plugin-feed
│  │  ├─gatsby-plugin-glamor
│  │  ├─gatsby-plugin-page-creator
│  │  ├─gatsby-plugin-sharp
│  │  ├─gatsby-remark-code-repls
│  │  ├─gatsby-source-filesystem
│  │  ├─gatsby-source-react-error-codes
│  │  ├─gatsby-transformer-authors-yaml
│  │  ├─gatsby-transformer-home-example-code
│  │  ├─gatsby-transformer-remark
│  │  ├─gatsby-transformer-sharp
│  │  ├─internal-data-bridge
│  │  ├─load-babel-config
│  │  └─prod-404
│  ├─commonjs
│  │      api-runner-browser-plugins.js
│  │      api-runner-browser.js
│  │      api-runner-ssr.js
│  │      api-ssr-docs.js
│  │      app.js
│  │      create-react-context.js
│  │      default-html.js
│  │      dev-loader.js
│  │      develop-static-entry.js
│  │      emitter.js
│  │      ensure-resources.js
│  │      error-overlay-handler.js
│  │      find-path.js
│  │      gatsby-browser-entry.js
│  │      json-store.js
│  │      loader.js
│  │      navigation.js
│  │      normalize-page-path.js
│  │      page-renderer.js
│  │      prefetch.js
│  │      production-app.js
│  │      public-page-renderer-dev.js
│  │      public-page-renderer-prod.js
│  │      public-page-renderer.js
│  │      react-lifecycles-compat.js
│  │      register-service-worker.js
│  │      root.js
│  │      socketIo.js
│  │      static-entry.js
│  │      strip-prefix.js
│  │
│  ├─fragments
│  │      image-sharp-fragments.js
│  │
│  ├─json
│  └─__tests__
│      │  .babelrc
│      │  dev-loader.js
│      │  error-overlay-handler.js
│      │  find-path.js
│      │  loader.js
│      │  minimal-config.js
│      │  static-entry.js
│      │  strip-prefix.js
│      │
│      └─__snapshots__
│              dev-loader.js.snap
│              loader.js.snap
│              static-entry.js.snap
│
├─.circleci
│      config.yml
│
├─.github
│      PULL_REQUEST_TEMPLATE.md
│
├─.idea
│  │  misc.xml
│  │  modules.xml
│  │  reactjs.org.iml
│  │  vcs.xml
│  │  workspace.xml
│  │
│  ├─codeStyles
│  │      codeStyleConfig.xml
│  │      Project.xml
│  │
│  └─inspectionProfiles
│          Project_Default.xml
│
├─content
│  │  404.md
│  │  acknowledgements.yml
│  │  authors.yml
│  │  footerNav.yml
│  │  headerNav.yml
│  │  languages.yml
│  │  versions.yml
│  │
│  ├─blog
│  │      2019-08-15-new-react-devtools.md
│  │
│  ├─community
│  │      articles.md
│  │
│  ├─docs
│  │      accessibility.md
│  │
│  ├─home
│  │  ├─examples
│  │  │      a-component-using-external-plugins.js
│  │  │      a-component-using-external-plugins.md
│  │  │      a-simple-component.js
│  │  │      a-simple-component.md
│  │  │      a-stateful-component.js
│  │  │      a-stateful-component.md
│  │  │      an-application.js
│  │  │      an-application.md
│  │  │
│  │  └─marketing
│  │          component-based.md
│  │          declarative.md
│  │          learn-once-write-anywhere.md
│  │
│  ├─images
│  │  │
│  │  ├─blog
│  │  │  │
│  │  │  ├─create-apps-with-no-configuration
│  │  │  │      compiled-successfully.png
│  │  │  │      compiled-with-warnings.png
│  │  │  │      created-folder.png
│  │  │  │      failed-to-compile.png
│  │  │  │      npm-run-build.png
│  │  │  │
│  │  │  ├─introducing-the-react-profiler
│  │  │  │      commit-selector.png
│  │  │  │      component-chart.png
│  │  │  │      devtools-profiler-tab.png
│  │  │  │      filtering-commits.gif
│  │  │  │      flame-chart.png
│  │  │  │      interactions-for-commit.png
│  │  │  │      interactions.png
│  │  │  │      navigate-between-interactions-and-commits.gif
│  │  │  │      no-interactions.png
│  │  │  │      no-profiler-data-multi-root.png
│  │  │  │      no-render-times-for-selected-component.png
│  │  │  │      no-timing-data-for-commit.png
│  │  │  │      props-and-state.gif
│  │  │  │      ranked-chart.png
│  │  │  │      see-all-commits-for-a-fiber.gif
│  │  │  │      see-which-props-changed.gif
│  │  │  │      select-a-root-to-view-profiling-data.gif
│  │  │  │      start-profiling.png
│  │  │  │      stop-profiling.png
│  │  │  │      zoom-in-and-out.gif
│  │  │  │
│  │  │  ├─react-v16.9.0
│  │  │  │      codemod.gif
│  │  │  │      cwm-warning.png
│  │  │  │
│  │  │  └─relay-components
│  │  │          relay-architecture.png
│  │  │          relay-containers-data-flow.png
│  │  │          relay-containers.png
│  │  │          sample-newsfeed.png
│  │  │
│  │  ├─docs
│  │  │      blur-popover-close.gif
│  │  │      cdn-cors-header.png
│  │  │      codewinds-004.png
│  │  │      devtools-dev.png
│  │  │      devtools-prod.png
│  │  │      error-boundaries-stack-trace-line-numbers.png
│  │  │      error-boundaries-stack-trace.png
│  │  │      granular-dom-updates.gif
│  │  │      implementation-notes-tree.png
│  │  │      javascript-jabber.png
│  │  │      keyboard-focus.png
│  │  │      outerclick-with-keyboard.gif
│  │  │      outerclick-with-mouse.gif
│  │  │      perf-dom.png
│  │  │      perf-exclusive.png
│  │  │      perf-inclusive.png
│  │  │      perf-wasted.png
│  │  │      react-devtools-state.gif
│  │  │      should-component-update.png
│  │  │      thinking-in-react-tagtree.png
│  │  │
│  │  └─tutorial
│  │          devtools.png
│  │          tictac-empty.png
│  │          tictac-numbers.png
│  │
│  ├─tutorial
│  │      nav.yml
│  │      tutorial.md
│  │
│  └─warnings
│          dont-call-proptypes.md
│          invalid-aria-prop.md
│          invalid-hook-call-warning.md
│          legacy-factories.md
│          refs-must-have-owner.md
│          special-props.md
│          unknown-prop.md
│
├─examples
│  │  .prettierrc
│  │  es5-syntax-example.js
│  │  hello-world.js
│  │  introducing-jsx.js
│  │  jsx-simple-example.js
│  │  reference-react-forward-ref.js
│  │  tutorial-expanded-version.js
│  │
│  ├─16-3-release-blog-post
│  │      context-example.js
│  │      create-ref-example.js
│  │      fancy-button-example.js
│  │      forward-ref-example.js
│  │      hoc-theme-example.js
│  │
│  ├─16-4-release-blog-post
│  │      pointer-events-example.js
│  │
│  ├─components-and-props
│  │      composing-components.js
│  │      extracting-components-continued.js
│  │      extracting-components.js
│  │      rendering-a-component.js
│  │
│  ├─context
│  │      motivation-problem.js
│  │      motivation-solution.js
│  │      multiple-contexts.js
│  │      reference-caveats-problem.js
│  │      reference-caveats-solution.js
│  │      theme-detailed-app.js
│  │      theme-detailed-theme-context.js
│  │      theme-detailed-themed-button.js
│  │      updating-nested-context-app.js
│  │      updating-nested-context-context.js
│  │      updating-nested-context-theme-toggler-button.js
│  │
│  ├─forwarding-refs
│  │      customized-display-name.js
│  │      fancy-button-ref.js
│  │      fancy-button-simple-ref.js
│  │      fancy-button-simple.js
│  │      fancy-button.js
│  │      log-props-after.js
│  │      log-props-before.js
│  │      wrapped-component-with-function-name.js
│  │      wrapped-component.js
│  │
│  ├─react-component-reference
│  │      get-snapshot-before-update.js
│  │
│  ├─reconciliation
│  │      index-used-as-key.js
│  │      no-index-used-as-key.js
│  │
│  ├─rendering-elements
│  │      render-an-element.js
│  │      update-rendered-element.js
│  │
│  ├─strict-mode
│  │      enabling-strict-mode.js
│  │      side-effects-in-constructor.js
│  │
│  ├─uncontrolled-components
│  │      input-type-file.js
│  │
│  └─update-on-async-rendering
│          adding-event-listeners-after.js
│          adding-event-listeners-before.js
│          adding-event-listeners-create-subscription.js
│          definition-getderivedstatefromprops.js
│          definition-getsnapshotbeforeupdate.js
│          fetching-external-data-after.js
│          fetching-external-data-before.js
│          initializing-state-after.js
│          initializing-state-before.js
│          invoking-external-callbacks-after.js
│          invoking-external-callbacks-before.js
│          react-dom-properties-before-update-after.js
│          react-dom-properties-before-update-before.js
│          side-effects-when-props-change-after.js
│          side-effects-when-props-change-before.js
│          updating-external-data-when-props-change-after.js
│          updating-external-data-when-props-change-before.js
│          updating-state-from-props-after.js
│          updating-state-from-props-before.js
│          using-react-lifecycles-compat.js
│
├─flow-typed
│      gatsby.js
│      glamor.js
│      hex2rgba.js
│      react-helmet.js
│      slugify.js
│
├─gatsby
│      createPages.js
│      onCreateNode.js
│      onCreatePage.js
│      onCreateWebpackConfig.js
│
├─plugins
│  ├─gatsby-remark-header-custom-ids
│  │      gatsby-client.js
│  │      gatsby-ssr.js
│  │      index.js
│  │      package.json
│  │
│  ├─gatsby-remark-use-jsx
│  │      index.js
│  │      package.json
│  │
│  ├─gatsby-source-react-error-codes
│  │      gatsby-node.js
│  │      package.json
│  │
│  ├─gatsby-transformer-authors-yaml
│  │      gatsby-node.js
│  │      package.json
│  │
│  ├─gatsby-transformer-home-example-code
│  │      gatsby-node.js
│  │      package.json
│  │
│  └─gatsby-transformer-versions-yaml
│          create-redirects.js
│          gatsby-node.js
│          package.json
│
├─public
│  │  external.png
│  │  favicon.ico
│  │  logo-og.png
│  │  robots.txt
│  │  search.svg
│  │  _redirects
│  │
│  ├─html
│  │      single-file-example.html
│  │
│  ├─js
│  │      jsfiddle-integration-babel.js
│  │      jsfiddle-integration.js
│  │
│  └─static
├─scripts
│      generateHeadingIDs.js
│
├─src
│  │  html.js
│  │  prism-styles.js
│  │  site-constants.js
│  │  theme.js
│  │  types.js
│  │
│  ├─components
│  │  ├─ButtonLink
│  │  │      ButtonLink.js
│  │  │      index.js
│  │  │
│  │  ├─CodeEditor
│  │  │      CodeEditor.js
│  │  │      index.js
│  │  │
│  │  ├─CodeExample
│  │  │      CodeExample.js
│  │  │      index.js
│  │  │
│  │  ├─Container
│  │  │      Container.js
│  │  │      index.js
│  │  │
│  │  ├─ErrorDecoder
│  │  │      ErrorDecoder.js
│  │  │      index.js
│  │  │
│  │  ├─Flex
│  │  │      Flex.js
│  │  │      index.js
│  │  │
│  │  ├─Header
│  │  │      Header.js
│  │  │      index.js
│  │  │
│  │  ├─Layout
│  │  │      index.js
│  │  │      Layout.js
│  │  │
│  │  ├─LayoutFooter
│  │  │      ExternalFooterLink.js
│  │  │      Footer.js
│  │  │      FooterLink.js
│  │  │      FooterNav.js
│  │  │      index.js
│  │  │      SectionLinks.js
│  │  │
│  │  ├─LayoutHeader
│  │  │      DocSearch.js
│  │  │      Header.js
│  │  │      HeaderLink.js
│  │  │      index.js
│  │  │      SearchSvg.js
│  │  │
│  │  ├─MarkdownHeader
│  │  │      index.js
│  │  │      MarkdownHeader.js
│  │  │
│  │  ├─MarkdownPage
│  │  │      index.js
│  │  │      MarkdownPage.js
│  │  │
│  │  ├─StickyResponsiveSidebar
│  │  │      index.js
│  │  │      StickyResponsiveSidebar.js
│  │  │
│  │  └─TitleAndMetaTags
│  │          index.js
│  │          TitleAndMetaTags.js
│  │
│  ├─css
│  │      algolia.css
│  │      reset.css
│  │
│  ├─icons
│  │      logo-white.svg
│  │      logo.svg
│  │
│  ├─images
│  │      oss_logo.png
│  │
│  ├─pages
│  │  │  404.js
│  │  │  acknowledgements.html.js
│  │  │  favicon.ico
│  │  │  index.js
│  │  │  jsx-compiler.html.js
│  │  │  languages.js
│  │  │  robots.txt
│  │  │  versions.js
│  │  │
│  │  ├─blog
│  │  │      all.html.js
│  │  │
│  │  └─docs
│  │          error-decoder.html.js
│  │
│  ├─templates
│  │  │  blog.js
│  │  │  codepen-example.js
│  │  │  community.js
│  │  │  docs.js
│  │  │  tutorial.js
│  │  │
│  │  └─components
│  │      ├─ChevronSvg
│  │      │      index.js
│  │      │
│  │      ├─ExternalLinkSvg
│  │      │      index.js
│  │      │
│  │      ├─MetaTitle
│  │      │      index.js
│  │      │
│  │      ├─NavigationFooter
│  │      │      index.js
│  │      │      NavigationFooter.js
│  │      │
│  │      └─Sidebar
│  │              index.js
│  │              ScrollSyncSection.js
│  │              Section.js
│  │              Sidebar.js
│  │
│  └─utils
│          createCanonicalUrl.js
│          createLink.js
│          findSectionForPath.js
│          isItemActive.js
│          loadScript.js
│          patchDOMForGoogleTranslate.js
│          sectionList.js
│          slugify.js
│          toCommaSeparatedList.js
│
└─static
    │  external.png
    │  favicon.ico
    │  logo-og.png
    │  robots.txt
    │  search.svg
    │  _redirects
    │
    ├─html
    │      single-file-example.html
    │
    └─js
            jsfiddle-integration-babel.js
            jsfiddle-integration.js


```
