## Responsive Frame

## Description
Window size tracking resizing components.

## Features
Responsive Frame follows the size changes of the window,
and the added Components also follow the size changes,
but it can also be specified in the traditional version.

## Gif
![alt text](https://github.com/MagyarZoli/ResponsiveFrame/blob/master/gif/giphy.gif)

## Example
Initialization, JFrame is passed to super() 
saving frame width and height dimensions. 
Additional components added to responsivePanel.
ComponentListener monitors the changes.
Construction of ResponsiveFrame counstrucktor:
```java
    public ResponsiveFrame(){
        super();
        this.frameWidth = this.getWidth();
        this.frameHeight = this.getHeight();
        super.add(responsivePanel);
        componentList();
        this.getContentPane().add(responsivePanel);
    }
```
Call componentListener and ComponentAdapter() abstract class to monitor window size changes.
specifying new Bounds for components
structure of componentResized:
```java
    private void componentList(){
        this.addComponentListener(new ComponentAdapter() {
            @Override
            public void componentResized(ComponentEvent e) {
                newBounds();
            }
        });
    }
```

## Authors
Magyar Zoltán

## Contact
magyarz95@gmail.com