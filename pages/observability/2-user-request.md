<StandardTab choosen="observability" />

<div class="h-full overflow-y-auto m-4">
  <div class="flex flex-row space-x-5">
    <div class="flex-1">
      <img src="https://www.positronx.io/wp-content/uploads/2019/09/react-login-ui-6748-02.png" class="h-72" />
    </div>
    <div class="flex-1 overflow-y-auto h-72">
      <h6 v-click>Uncertainty</h6>
      <span v-after class="text-xs">Based on data</span>
      <ul class="text-xs font-extralight mt-5">
        <li v-click>Bagaimana cara kita bisa mengetahui problem yang terjadi pada apps ?</li>
        <li class="!ml-8 font-semibold" v-click>Melalui user report</li>
        <li v-click>Bagaimana jika ada bug yang krusial terjadi disistem tetapi kita terlambat mengetahuinya ?</li>
        <li class="!ml-8 font-semibold" v-click>Kirim pesan error ke client atau maintainer</li>
        <li v-click>Bagaimana cara bisa menyelesaikan bug dengan cepat ?</li>
        <li class="!ml-8 font-semibold" v-click>Buat pesan error yang jelas dalam sistem</li>
      </ul>
    </div>
  </div>
</div>

<!--
Time: 28:00

- tahap ini kita akan melakukan integrasi dengan 3rd party seperti sentry, rocketlog, dsb
- yang harus kita pastikan adalah error messagenya clear
- untuk case-case tadi adalah error yang sudah dihandle
- yang belum kita perhitungkan adalah unhandled error seperti rate limit, database connection error, dsb
-->