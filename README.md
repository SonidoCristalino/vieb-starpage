# Startpage

An iTerm-inspired startpage page for faster web browsing through Vieb. Because everything's better on
keyboard!. 

This project is based on [Start Page](https://github.com/peterrauscher/startpage)

![Screenshot](/Screenshot.png)

## Installation

You have only one option to use this page with [Vieb](https://vieb.dev/download)

1. ### Local File

   - To run locally, you can simply clone the repository:

     ```bash
     git clone https://github.com/SonidoCristalino/vieb-starpage
     ```
2. **WARNING**: After download, you must change the dir name from `vieb-startpage` to simply `startpage`. 
3. Now just set your `newtaburl` option in Vieb as `/path/startpage/index.html`. 

## Usage

1. First thing you have to do is set your `/path/startpage/index.html` in your `newtaburl` setting. 
2. This could be done througth set command: `set newtaburl="/path/startpage/index.html"`
3. If you are satisfy with results, then save it with `mkviebrc`. 
4. Others useful options could be found here: [Start Page](https://github.com/peterrauscher/startpage)

## Configuration

Because this is a static site, configuration mostly happens within the files themselves. Some things, like the weather API key and location, are stored in local storage. If you completely clear your browser, you will need to reset these.

### Shortcuts

Shortcuts are the links displayed when you first open the page, or when you run `ls`. These are defined in the `js/shortcuts.js` file.

The file is an array of objects of the schema:

```
{
  category: "Name of Category",
  color: "color of category header",
  items: {
    "Example": "https://example.com",
    "Another Example": "https://anotherexample.com",
    ...
  }
}
```

Feel free to add/remove categories and links.

Available values for `color` are:

- `green`
- `cyan`
- `purple`
- `red`
- `yellow`
- `blue`
- `light-gray`
- `gray`
- `black`

### Username and Hostname

Just change the text in `index.html`:

```html
<div class="prompt">
  ...
  <span class="green">username</span>
  ...
  <span class="cyan">hostname</span>
  ...
</div>
```
