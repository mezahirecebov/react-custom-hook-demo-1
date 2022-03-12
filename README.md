#REACT CUSTOM HOOK DEMO

_useCounter_

const useCounter = (x) => {
const [counter, setCounter] = useState(0);

useEffect(() => {
const interval = setInterval(() => {
setCounter((prevCounter) => prevCounter + x);
}, 1000);

    return () => clearInterval(interval);

}, [x]);

return counter;
};
