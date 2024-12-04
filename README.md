# React useEffect Hook Runs on Every Render
This repository demonstrates a scenario where a React `useEffect` hook with an empty dependency array runs on every render. This is a subtle issue that can lead to unexpected behavior and performance problems. The issue arises from the fact that even with an empty dependency array, the effect can still run when the component re-renders due to closure issues. In this particular case, it occurs when the function component is deeply nested or has other states that change frequently which causes a stale closure. 

## Steps to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs showing that the effect runs more than once.