<StandardTab choosen="security" />

<div class="my-4"></div>

<h6>Data Requirement</h6>

<div class="h-full overflow-y-auto m-4">
  <div class="overflow-x-auto relative shadow-md sm:rounded-lg">
    <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
      <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
        <tr>
          <th scope="col" class="py-3 px-6">
            Column
          </th>
          <th scope="col" class="py-3 px-6">
            Type
          </th>
          <th scope="col" class="py-3 px-6">
            Validation
          </th>
          <th scope="col" class="py-3 px-6">
            Relation
          </th>
        </tr>
      </thead>
      <tbody>
        <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
          <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
            firstName
          </th>
          <td class="py-4 px-6">
            string
          </td>
          <td class="py-4 px-6">
          </td>
          <td class="py-4 px-6">
            -
          </td>
        </tr>
        <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
          <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
            lastName
          </th>
          <td class="py-4 px-6">
            string
          </td>
          <td class="py-4 px-6">
          </td>
          <td class="py-4 px-6">
            -
          </td>
        </tr>
        <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
          <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
            email
          </th>
          <td class="py-4 px-6">
            string
          </td>
          <td class="py-4 px-6">
            required, <span class="font-bold">unique</span>
          </td>
          <td class="py-4 px-6">
            -
          </td>
        </tr>
        <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
          <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
            password
          </th>
          <td class="py-4 px-6">
            string
          </td>
          <td class="py-4 px-6">
            required, <span class="font-bold">min 8 digit,<br/> should contains alphanumeric + symbol</span>
          </td>
          <td class="py-4 px-6">
            -
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<!--
Time: 13:00

- ternyata setelah menambahkan concern about security, ada perubahan di requirement yang perlu penyesuaian dalam code juga
-->