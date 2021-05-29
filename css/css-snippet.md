# css snippet



마지막 child를 제외하고 margin-right 값 주기

```css
ul li :not(:last-child) {
    margin-right: 5px;
}
```

```jsx
const Group = styled.ul`
    & > li:not(:last-child) {
        margin-right: 5px;
    }
`
```

