---
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Getting Started

Creating an Analog project can be done with minimal steps.

## System Requirements

Analog requires the following Node and Angular versions:

- Node v18.13.0 and higher is recommended
- Angular v15 or higher

## Creating a New Application

To create a new Analog project, you can use the `create-analog` package with your package manager of choice:

<Tabs groupId="package-manager">
  <TabItem value="npm">

```shell
npm create analog@latest
```

  </TabItem>

  <TabItem label="Yarn" value="yarn">

```shell
yarn create analog
```

  </TabItem>

  <TabItem value="pnpm">

```shell
pnpm create analog
```

  </TabItem>
  <TabItem value="bun">

```shell
bun create analog
```

  </TabItem>
</Tabs>

You can also [scaffold a new project with Nx](/docs/integrations/nx).

### Serving the application

To start the development server for the application, run the `start` command.

<Tabs groupId="package-manager">
  <TabItem value="npm">

```shell
npm run start
```

  </TabItem>

  <TabItem label="Yarn" value="yarn">

```shell
yarn start
```

  </TabItem>

  <TabItem value="pnpm">

```shell
pnpm start
```

  </TabItem>
  <TabItem value="bun">

```shell
bun start
```

  </TabItem>
</Tabs>

Visit [http://localhost:5173](http://localhost:5173) in your browser to view the running application.

Next, you can [define additional routes using components](/docs/features/routing/overview) for navigation.

### Building the Application

To build the application for deployment

<Tabs groupId="package-manager">
  <TabItem value="npm">

```shell
npm run build
```

  </TabItem>

  <TabItem label="Yarn" value="yarn">

```shell
yarn build
```

  </TabItem>

  <TabItem value="pnpm">

```shell
pnpm run build
```

  </TabItem>
  <TabItem value="bun">

```shell
bun run build
```

  </TabItem>
</Tabs>

### Build Artifacts

By default, Analog comes with [Server-Side Rendering](/docs/features/server/server-side-rendering) enabled.
Client artifacts are located in the `dist/analog/public` directory.
The server for the API/SSR build artifacts is located in the `dist/analog/server` directory.

## Migrating an Existing Application

You can also migrate an existing Angular application to Analog. See the [migration guide](/docs/guides/migrating) for migration steps.

## Mermaid Examples

### Example 1

```mermaid
block-beta
columns 1
  db(("DB"))
  blockArrowId6<["&nbsp;&nbsp;&nbsp;"]>(down)
  block:ID
    A
    B["A wide one in the middle"]
    C
  end
  space
  D
  ID --> D
  C --> D
  style B fill:#969,stroke:#333,stroke-width:4px
```

### Example 2

```mermaid
block-beta
  columns 3
  a:3
  block:group1:2
    columns 2
    h i j k
  end
  g
  block:group2:3
    %% columns auto (default)
    l m n o p q r
  end  
```

### Example 3

```mermaid
block-beta
  id1[/"This is the text in the box"/]
  id2["This is the text in the box"]
  A[/"Christmas"]
  B["Go shopping"/]
```

### Example 4

```mermaid
block-beta
  blockArrowId<["Label"]>(right)
  blockArrowId2<["Label"]>(left)
  blockArrowId3<["Label"]>(up)
  blockArrowId4<["Label"]>(down)
  blockArrowId5<["Label"]>(x)
  blockArrowId6<["Label"]>(y)
  blockArrowId6<["Label"]>(x, down)
```

### Example 5

```mermaid
block-beta
  columns 3
  Start(("Start")) space:2
  down<[" "]>(down) space:2
  Decision("Make Decision") right<["Yes"]>(right) Process1["Process A"]
  downAgain<["No"]>(down) space r3<["Done"]>(down)
  Process2["Process B"] r2<["Done"]>(right) End(("End"))

  style Start fill:#969;
  style End fill:#696;
```

### Example 6

```mermaid
graph LR
  B("$$\begin{array} {lcl} L(p,w_i) &=& \dfrac{1}{N}\Sigma_{i=1}^N(\underbrace{f_r(x_2 \rightarrow x_1 \rightarrow x_0)G(x_1 \longleftrightarrow x_2)f_r(x_3 \rightarrow x_2 \rightarrow x_1)}_{sample\, radiance\,evaluation\, in\, stage2} \\\\\\ &=& \prod_{i=3}^{k-1}(\underbrace{\dfrac{f_r(x_{i+1} \rightarrow x_i \rightarrow x_{i-1})G(x_i \longleftrightarrow x_{i-1})}{p_a(x_{i-1})}}_{stored\,in\,vertex\, during\,light\, path\, tracing\, in\, stage1})\dfrac{G(x_k \longleftrightarrow x_{k-1})L_e(x_k \rightarrow x_{k-1})}{p_a(x_{k-1})p_a(x_k)}) \end{array}$$")
  A-->B
```

### Example 7

```mermaid
graph LR
  B("$$\sqrt{\frac{\pi(1-\pi)}{n}}$$")
  A-->B
```
