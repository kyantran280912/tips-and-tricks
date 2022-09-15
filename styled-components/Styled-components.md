# Tips and tricks Styled-components

## Using JavaScript to out advantage (Sử dụng JavaScript để tạo lợi thế)

#### To make a line overflow with an ellipsis (…) when the text is longer than the container element is wide, you need three CSS properties: (Khi chữ tràn sẽ có dấu (...) nếu dài quá width của vùng chứa:)

```css
.box-text {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```
