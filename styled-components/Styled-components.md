# Tips and tricks Styled-components

##### A collection of useful tips and tricks when working with styled-components! (Bộ sưu tập mẹo và các thủ thuật khi làm việc với Styled-componets)!

## Using JavaScript to out advantage (Sử dụng JavaScript để tạo lợi thế)

##### To make a line overflow with an ellipsis (…) when the text is longer than the container element is wide, you need three CSS properties: (Khi chữ tràn sẽ có dấu (...) nếu dài quá width của vùng chứa)

```css
.box-text {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

##### You could create a separate component for truncating, but in this case reusing the CSS might not be a bad idea! Instead of hardcoding those lines of code in every component you want to truncate though, you could write a function that does it for you: (Sử dụng function để tạo những thành phần riêng CSS để sử dụng lại và có thể thay đổi Width hoặc bất cứ thành phần CSS nào)

```js
export function truncate(width) {
  return `
    width: ${width};
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  `;
}
```

##### Then you can use it like this:(Sau đó bạn có thể sử dụng như sau)

```js
import { truncate } from "../style-utils";

// Make this div truncate the text with an ellipsis
const Box = styled.div`
  ${truncate("250px")}
  background: papayawhip;
`;
```
