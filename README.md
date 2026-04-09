# goit-js-hw-08

Final homework assignment of the course

Create a repository `goit-js-hw-08`.
Complete the task in the files `gallery.js` and `index.html`.

> **Note!** File and folder names, as well as their nesting structure, must match the specified scheme. Otherwise, the work will not be accepted.

- Read the task and complete it in the code editor.
- Make sure the code is formatted using Prettier and there are no errors or warnings in the console when opening the live page of the task.
- Submit the homework for review.

## Submission format

- The homework contains two links: to the source files (link to the repository with the code) and to the live page on GitHub Pages.
- Attached repository file in zip format.

> ☝ **IMPORTANT**
> Read the [Instructions on uploading a working file from the repository to GitHub](#).

## Grading format

- Score from 0 to 100.

Use this layout for styling your task markup.

---

## Task. Image Gallery

Create a gallery with the ability to click on its elements and view a full-size image in a modal window. Watch the demo video of the gallery's operation.

Creating a gallery is a complex task that is best broken down into several simpler subtasks; by completing each one, you will get closer to the final goal. This process is called task decomposition.

### 1. Gallery markup

It is logical to start by creating the place where we will add gallery elements. To do this, add a gallery container tag in the HTML code — an unordered list with the class `gallery`.

```html
<ul class="gallery"></ul>
```

### 2. Image array

To create gallery elements, you will need data. Add this array of objects to your JavaScript file. Each object represents one gallery element.

- `preview` — link to the small version of the image for the gallery card
- `original` — link to the large version of the image for the modal window
- `description` — text description of the image, for the `alt` attribute of the small image and the caption of the large image in the modal.

```js
const images = [
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820__480.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820_1280.jpg',
    description: 'Hokkaido Flower',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677_1280.jpg',
    description: 'Container Haulage Freight',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/16/09/47/beach-4206785__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/16/09/47/beach-4206785_1280.jpg',
    description: 'Aerial Beach View',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2016/11/18/16/19/flowers-1835619__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2016/11/18/16/19/flowers-1835619_1280.jpg',
    description: 'Flower Blooms',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2018/09/13/10/36/mountains-3674334__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2018/09/13/10/36/mountains-3674334_1280.jpg',
    description: 'Alpine Mountains',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/16/23/04/landscape-4208571__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/16/23/04/landscape-4208571_1280.jpg',
    description: 'Mountain Lake Sailing',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/17/09/27/the-alps-4209272__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/17/09/27/the-alps-4209272_1280.jpg',
    description: 'Alpine Spring Meadows',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/16/21/10/landscape-4208255__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/16/21/10/landscape-4208255_1280.jpg',
    description: 'Nature Landscape',
  },
  {
    preview:
      'https://cdn.pixabay.com/photo/2019/05/17/04/35/lighthouse-4208843__340.jpg',
    original:
      'https://cdn.pixabay.com/photo/2019/05/17/04/35/lighthouse-4208843_1280.jpg',
    description: 'Lighthouse Coast Sea',
  },
];
```

### 3. Gallery elements markup

You have a container to which you can add gallery elements, and data from which they can be created. It's time to fill the gallery with markup.

Use the `images` array of objects and this HTML template of a gallery element to create the markup of elements in JavaScript code, and then add all the markup inside `ul.gallery`. Do not add other HTML tags besides those contained in this template.

```html
<li class="gallery-item">
  <a class="gallery-link" href="large-image.jpg">
    <img
      class="gallery-image"
      src="small-image.jpg"
      data-source="large-image.jpg"
      alt="Image description"
    />
  </a>
</li>
```

- In the `src` attribute of the `<img>` tag, specify the link to the small version of the image.
- For the `alt` attribute, use the image description.
- The link to the large image must be stored in the `data-source` attribute on the `<img>` element, and specified in the `href` of the link.
- Note that the image is wrapped in a link whose `href` attribute points to the path of the image file. So clicking on it can trigger downloading the image to the user's computer. Prevent this default behavior.

### 4. Styles

Add gallery styling according to the layout.

### 5. Delegation

It's time to add the functionality of listening for clicks on gallery elements and getting the link to the large image on click. To do this, use the delegation technique on `ul.gallery`. For now, on clicking a gallery element, output the link to the large image to the console.

### 6. Connecting the library

The `basicLightbox` library represents a fully functional modal window that perfectly suits our task. Use the `jsdelivr` CDN service and add links to the minified (.min) JS and CSS files of the library to the HTML file.

### 7. Modal window

Supplement your code so that clicking on a gallery element opens the modal window of the connected library. To learn how to initialize a modal window in your code and how to use it, read the documentation and examples.

### 8. Large image

Use your code for getting the link to the large image to replace the value of the `src` attribute of the `<img>` element in the modal window before opening. Use the ready-made markup of the modal window with an image from the `basicLightbox` library examples.

---

## What the mentor will pay attention to during the review:

- The live page displays the image gallery from the `images` data array.
- The image gallery is styled according to the layout.
- The data for the gallery is created dynamically in JS.
- When listening for the click event on gallery elements, the delegation technique is used.
- When clicking between gallery elements, nothing happens.
- The `basicLightbox` library is connected.
- When clicking on a gallery element, a modal window of the connected library opens, containing an enlarged version of the image that was clicked.
