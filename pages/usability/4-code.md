<StandardTab choosen="usability" />

<div class="my-4"></div>

<div class="flex items-end space-x-5">
  <h6>Code Implementation</h6>
  <span class="text-sm text-gray-400">Define data model</span>
</div>

<div class="h-96 overflow-y-auto my-4">
```ts {all|2|3,4|5,6|all}
interface User {
  id: number // auto generate number
  firstName?: string // optional
  lastName?: string // optional
  email: string
  password: string
}
```
</div>

<!--
Time: 08:00

- Code sesuai ekspektasi (data)
-->