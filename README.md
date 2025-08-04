# mlue
 Reactive Programming With Style

```JavaScript

// The Basic Idea:

globalThis.rev = new Revision(7);

class Rectangle {
  constructor(width, height) {

    this.rev new Revision();
    this.width = width;
    this.height = height;

    return Revision.watcher(this, ['width', 'height']);
  }

  // Instance method
  getArea() {
    return this.width * this.height;
  }

  // Static method
  static compareArea(rect1, rect2) {
    return rect1.getArea() - rect2.getArea();
  }

}

let rect1 = new Rectangle(5, 8);
let rect2 = new Rectangle(6, 7);

console.log(Rectangle.compareArea(rect1, rect2)); // -2


Revision.watch(globalThis.rev, rect1.rev, rect2.rev)
.subscribe(()=>console.log(Rectangle.compareArea(rect1, rect2)))


rect1.height = 77;
rect1.rev.inc();

```
