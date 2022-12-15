<StandardTab choosen="usability" />

<div class="my-4"></div>

<h6>Api Docs Concept</h6>

<div class="h-full overflow-y-auto my-4">
  <div class="flex flex-col space-y-5 overflow-x-auto relative shadow-md sm:rounded-lg">
    <div>
      <h5 class="font-extralight">ENDPOINT URL</h5>
      <span class="text-sm">www.example.com/register</span>
    </div>
    <div>
      <h5 class="font-extralight">INPUT</h5>
      <div class="overflow-y-auto my-4">
```ts
const form = {
  firstName: ''
  lastName: ''
  email: 'johndoe@example.com'
  password: 'mypassword'
}
```
      </div>
    </div>
    <div>
      <h5 class="font-extralight">OUTPUT</h5>
      <span class="text-xs mt-5">Success</span>
      <div class="overflow-y-auto mb-5">
```ts
{
  _id: '$autoGenerateId123456'
}
```
      </div>
      <span class="text-xs mt-5">Failed</span>
      <div class="overflow-y-auto mb-20">
```ts
{
  error: {
    code: 422,
    message: 'Unprocessable Entity'
    errors: {
      'email': 'email is required',
      'password': 'password is required'
    }
  }
}
```
      </div>
    </div>
  </div>
</div>

<!--
Time: 07:00

- Apa yang terjadi ketika proses registrasi
- client memanggil url atau endpoint
- client memberikan input
- client menerima output
-->