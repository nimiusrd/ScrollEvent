# ScrollEvent

## Windowのscrollイベントを捕捉し，座標を取得

```js
window.addEventListener('scroll', event => {
    console.log('x:', window.scrollX)
    console.log('y:', window.scrollY)
})
```

## 要素のscrollイベントを捕捉し，座標を取得

```js
elem.addEventListener('scroll', event => {
    console.log('x:', event.target.scrollLeft)
    console.log('y:', event.target.scrollTop)
})
```

このとき取得できるのは要素の左上を(0, 0)とした相対座標．

## 要素のscrollイベントを捕捉し，スクロールの割合を求める

```js
elem.addEventListener('scroll', event => {
    const dx = event.target.scrollLeft / (event.target.scrollWidth - event.target.clientWidth)
    const dy = event.target.scrollTop / (event.target.scrollHeight - event.target.clientHeight)
    console.log('dx:', dx)
    console.log('dy:', dy)
```

