# Tips and tricks Styled-components
##### A collection of useful tips and tricks when working with styled-components! (Bộ sưu tập mẹo và các thủ thuật khi làm việc với Styled-componets)!

## Using JavaScript to out advantage (Sử dụng JavaScript để tạo lợi thế)

##### To make a line overflow with an ellipsis (…) when the text is longer than the container element is wide, you need three CSS properties: (Khi chữ tràn sẽ có dấu (...) nếu dài quá width của vùng chứa:)

```css
.box-text {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```
