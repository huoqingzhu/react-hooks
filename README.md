### react

## 创建项目

npx create-react-app hook-ts-demo --template typescript

### hooks

1. useState 生成响应式数据
2. useEffect (React 会保存你传递的函数（我们将它称之为 “effect”），并且在执行 DOM 更新之后调用它)
   useEffect 的第二参数 是绑定一个参数 或者多个参数 这个参数变化才执行操作
   useEffect 可以返回一个函数 可以实现清除机制
   useEffect 可以理解为于vue的 watch 功能

3.Hook 使用规则
✅ 在 React 的函数组件中调用 Hook
✅ 在自定义 Hook 中调用其他 Hook
❌不要在循环，条件或嵌套函数中调用 Hook
4. 自定义hook
   ✅dui自定义 Hook 必须以 “use” 开头

   ❌在两个组件中使用相同的 Hook 会共享 state

5. useContext
   1. 帮助我们跨越组件层级直接传递变量，实现共享
   2. 父组件传子组件

6. useReducer
  1.类似reducer
  2。配合useContext可实现全局数据共享

7. useRef
   1. 获取ref的组件
   2. 它还相当于 this , 可以存放任何变量，很好的解决闭包带来的不方便性。

8. useMemo（比useEffect更细腻）
   1. useMemo 的函数会在渲染期间执行
   2. useMemo可以减少页面开销提高性能

9.useCallback
  1.  useCallback 返回的是函数
  2.  useCallback和React.memo必须结合使用