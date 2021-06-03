# Component 정의



```typescript
interface List2Props extends Omit<HTMLAttributes<HTMLDivElement>, 'title'> {
  title: React.ReactElement;
  caption?: React.ReactElement;
  rightIcon?: React.ReactElement;
  onClick?: React.MouseEventHandler<HTMLDivElement>;
}

export const List2 = memo<List2Props>(({ title, caption, rightIcon, onClick: handleOnclick, ...props }) => {
  return (
    <List2Container {...props} onClick={handleOnclick}>
            ../
    </List2Container>
  );
});

```

event, aria-\*, data-\* 등도 받을 수 있어야 한다.

  


