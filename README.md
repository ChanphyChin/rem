```javascript
  /**
   * @author Chanphy
   * @description 以标准设计稿750为参照，1rem换算为100px;其余尺寸按照该尺寸进行换算
   */
  (function(d, w) {
      const doc = d.documentElement;
      function rem() {
        const width = Math.min(doc.getBoundingClientRect().width, 750);
        doc.style.fontSize = width / 3.75 + 'px';
      }
      rem();
      w.addEventListener('resize', rem);
  })(document, window);
```
