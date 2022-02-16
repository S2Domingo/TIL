# Cascading & Specificity

HTML elemets는 어떤 스타일을 적용할지에 대한 우선순위, Cascading이 있다. 중요도와 명시도가 높은 것을 우선적으로 적용한다.

## Specificity
!important > inline sytle sheet > an id selector > a class or pseudo or attribute selector > an element(tag) selector > inherited style

## Order of importance
1. !important
2. Author inline style style sheet: 적용하고자 하는 element 내의 `style = `
```
<p style = "color: black">
Yes
</p>
```
3. Author embedded or Internal style sheet: `<head>` section 내의 `<style>`
4. Author external style sheet: `<link>`로 연결된 CSS파일 내의 style
5. User style sheet
6. Default Browser  style sheet 


## Override
명시도가 똑같을 때는, 나중에 선언된 것이 적용된다. 

[source](https://www.plus2net.com/html_tutorial/css-types.php#:~:text=types%20of%20CSS.-,Inline%20style,Internal%20and%20external%20defined%20styles)