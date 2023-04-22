# React Fetch API Hook
Simple hook to use the Fetch API in react for ajax calls.

## Sample Usage
```
const { post, get } = useFetch();

const getHome = await post({uri: '/pages/home', data: {someparam: 1}});

try {
  response = await get({uri: '/header', data: {someparam: 1}, errors: true);
} catch(err) {
  const error = err as ajaxErrorResponse<{message: string;}>
  console.log(error.status, errors.statusText, error.body.message);
}
```
If you omit errors: true the error will be catched by the hook, for things you don't need to handle manually.
