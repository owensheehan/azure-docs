---
author: laujan
ms.service: cognitive-services
ms.topic: include
ms.date: 03/27/2020
ms.author: lajanuar
ms.custom: devx-track-js
---

:::row:::
    :::column span="3":::
        The Speech SDK for JavaScript is available as an npm package, see <a href="https://www.npmjs.com/package/microsoft-cognitiveservices-speech-sdk" target="_blank">microsoft-cognitiveservices-speech-sdk </a> and its companion GitHub repository <a href="https://github.com/Microsoft/cognitive-services-speech-sdk-js" target="_blank">cognitive-services-speech-sdk-js </a>.
    :::column-end:::
    :::column:::
        <br>
        <div class="icon is-large">
            <img alt="JavaScript" src="https://docs.microsoft.com/media/logos/logo_js.svg"  width="60px">
        </div>
    :::column-end:::
:::row-end:::

> [!TIP]
> Although the Speech SDK for JavaScript is available as an npm package, thus both client web browsers and Node.js can consume it - consider the various architectural implications of each environment. For example, the <a href="https://en.wikipedia.org/wiki/Document_Object_Model" target="_blank">document object model (DOM) </a> is not available for server-side applications just as the <a href="https://nodejs.org/api/fs.html" target="_blank">file system </a> is not available to client-side applications.

### Node.js Package Manager (NPM)

To install the Speech SDK for JavaScript, run the following `npm install` command below.

```nodejs
npm install microsoft-cognitiveservices-speech-sdk
```

### HTML script tag

Alternatively, you could directly include a `<script>` tag in the HTMLs `<head>` element, relying on the <a href="https://www.jsdelivr.com/package/npm/microsoft-cognitiveservices-speech-sdk" target="_blank">**JSDelivr** NPM syndicate </a>.

```html
<script src="https://cdn.jsdelivr.net/npm/microsoft-cognitiveservices-speech-sdk@latest/distrib/browser/microsoft.cognitiveservices.speech.sdk.bundle-min.js">
</script>
```

For more information, see the <a href="https://github.com/Azure-Samples/cognitive-services-speech-sdk/tree/master/quickstart/javascript/browser" target="_blank">Web Browser Speech SDK quickstart </a>.
