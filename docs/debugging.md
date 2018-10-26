Debugging extensions is easier on Sourcegraph.com than on GitHub.com via the browser extension, so open up a file such as https://sourcegraph.com/github.com/gorilla/mux/-/blob/mux.go

First, make sure your extension is active by opening your browser developer tools and running `localStorage.debug=true` and refreshing the page. You should see a little Ext debug button:

![](https://user-images.githubusercontent.com/1387653/47594902-54da8780-d932-11e8-8180-639b4e09c683.png)

Turning on "Log to devtools console" will show messages being passed back and forth such as:

![](https://user-images.githubusercontent.com/1387653/47594934-80f60880-d932-11e8-8cf4-eccc31433c32.png)

`console.log` statements in your Sourcegraph extension will show up in the developer tools pane in your browser.

You can set breakpoints by first finding your Sourcegraph extension script that's running in a web worker:

![](https://user-images.githubusercontent.com/1387653/47594858-278dd980-d932-11e8-976d-4f49a5a2953f.png)

