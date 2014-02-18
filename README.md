## About

This is an implementation of currentPageIndicatorTintColor and pageIndicatorTintColor for ScrollableView and allowsInlineMediaPlayback for WebView on Titanium SDK 3.2.1.GA

## Installation

Replace `TiUIScrollableView.h`, `TiUIScrollableView.m`, `TiUIScrollableViewProxy.h`, `TiUIScrollableViewProxy.m` and `TiUIWebView.m` in `~/Library/Application Support/Titanium/mobilesdk/osx/3.2.1.GA/iphone/Classes` with the files provided.

## Usages

### IndicatorTintColor
You can now use pageIndicatorTintColor and currentPageIndicatorTintColor to set the color of the Indicators on the Ti.UI.createScrollableView
#### Example:
```javascript
var theScrollableView = Ti.UI.createScrollableView({
	width : 'auto',
	height : 'auto',
	backgroundColor : 'transparent',
	showPagingControl : true,
	pagingControlHeight : 30,
	pagingControlColor : 'transparent',
	pageIndicatorTintColor : 'gray', //Indicator Color
	currentPageIndicatorTintColor : 'black', //Active Indicator Color
	overlayEnabled : true, //Add Pagination as an Overlay to View
});
```

### allowsInlineMediaPlayback
In order for video to play inline on WebViews, the video element in the HTML document must also include the `webkit-playsinline` attribute.
#### Example:
```html
<iframe webkit-playsinline width="320" height="180" src="https://www.youtube.com/embed/gBWwP6cmk5Q?rel=0&playsinline=1" frameborder="0"></iframe>
```
PS: For Youtube HTML5 player you need to use the parameter `playsinline=1` as specified on `https://developers.google.com/youtube/player_parameters#playsinline`

#### Clean and rebuild your project to have it working.
