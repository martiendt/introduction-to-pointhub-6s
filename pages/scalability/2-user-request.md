<StandardTab choosen="scalability" />

<div class="h-full overflow-y-auto m-4">
  <div class="flex flex-row space-x-5">
    <div class="flex-1">
      <img src="https://i.ibb.co/Jjk2T8t/signup.png" class="h-72" />
    </div>
    <div class="flex-1 overflow-y-auto h-72">
      <h6 v-click>Scalability Issue</h6>
      <span v-after class="text-xs">Think about large codebase, users, and database</span>
      <ul class="text-xs font-extralight mt-10">
        <li v-click>Bagaimana jika client butuh customize apps nya ?</li>
        <li v-click>Bagaimana jika mau diintegrasikan dengan apps yang sudah ada ?</li>
        <li v-click>Bagaimana jika ada 1000 user akses ke web aplikasi secara bersamaan ?</li>
        <li v-click>Apakah jika ada jutaan data didatabase akan mempengaruhi performance speed load time ?</li>
      </ul>
    </div>
  </div>
</div>

<!--
Time: 29:00

- kita perlu penerapan design principles seperti clean code architecture, bridge pattern, dsb supaya agility atau proses coding bisa lebih efisien
- query example yang tidak efisien sehingga menjadi bottleneck load time
- hal-hal tersebut akan kita solve case by case menggunakan best practice coding dan design principles
-->