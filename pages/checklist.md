<h3 class="font-extrabold">Checklist</h3>

<div class="h-full overflow-y-auto my-4">
  <ul class="text-xs font-extralight mt-5">
    <li v-click>Apakah semua data harus diisi ?</li>
    <li class="!ml-8 font-semibold" v-after>Hanya email dan password yang wajib diisi</li>
    <li v-click>Apa yang terjadi jika data yang diperlukan tidak diisi ?</li>
    <li class="!ml-8 font-semibold" v-after>Proses registrasi akan gagal, dan user diberikan info kenapa gagal</li>
    <li v-click>Apa yang terjadi setelah tombol "Sign Up" ditekan ?</li>
    <li class="!ml-8 font-semibold" v-after>Proses registrasi berhasil akan kirim notifikasi & verifikasi email</li>
    <li class="!ml-8 font-semibold" v-after>Proses registrasi gagal akan kirim notifikasi gagal</li>
    <li v-click>Bagaimana jika user daftar menggunakan email yang sama ?
    </li>
    <li class="!ml-8 font-semibold" v-after>1 email hanya bisa digunakan 1x pendaftaran</li>
    <li class="!ml-8 font-semibold" v-after>Kirim notifikasi bahwa email sudah pernah digunakan</li>
    <li v-click>Bagaimana jika ada orang yang mau meretas akun orang lain dengan cara mencoba-coba terus dengan random password ?</li>
    <li class="!ml-8 font-semibold" v-after>User yang mendaftar harus membuat strong password</li>
    <li class="!ml-8 font-semibold" v-after>Min 8 digit dan terdiri dari huruf, angka dan simbol</li>
    <li v-click>Bagaimana jika programmer atau admin server kita melihat data password yang disimpan ?</li>
    <li class="!ml-8 font-semibold" v-after>Password yang disimpan harus dienkripsi</li>
    <li v-click>Bagaimana cara programmer lain paham dengan code saya ?</li>
    <li class="!ml-8 font-semibold" v-after>Dokumentasi</li>
    <li class="!ml-8 font-semibold" v-after>Simplify the code dengan penerapan design principles</li>
    <li class="!ml-8 font-semibold" v-after>Konsistensi format penulisan code (eslint, prettier)</li>
    <li v-click>Bagaimana cara supaya code dapat dipahami hanya dengan 1x baca ?</li>
    <li class="!ml-8 font-semibold" v-after>Single Responsibility Principle</li>
    <li class="!ml-8 font-semibold" v-after>Hindari nested if else statement</li>
    <li v-click>Bagaimana jika programmer lain menyebabkan apps yang sudah jalan dengan baik menjadi bug ?</li>
    <li class="!ml-8 font-semibold" v-after>It can be tested at the code level (dapat dipastikan kebenarannya oleh sistem, bukan hanya human test)</li>
    <li class="!ml-8 font-semibold" v-after>Unit Testing</li>
    <li class="!ml-8 font-semibold" v-after>Integration Testing</li>
    <li class="!ml-8 font-semibold" v-after>e2e Testing</li>
    <li v-click>Bagaimana cara kita bisa mengetahui problem yang terjadi pada apps ?</li>
    <li class="!ml-8 font-semibold" v-after>Melalui user report</li>
    <li v-click>Bagaimana jika ada bug yang krusial terjadi disistem tetapi kita terlambat mengetahuinya ?</li>
    <li class="!ml-8 font-semibold" v-after>Kirim pesan error ke client atau maintainer</li>
    <li v-click>Bagaimana cara bisa menyelesaikan bug dengan cepat ?</li>
    <li class="!ml-8 font-semibold" v-after>Buat pesan error yang jelas dalam sistem</li>
    <li v-click>Bagaimana jika client butuh customize apps nya ?</li>
    <li v-click>Bagaimana jika mau diintegrasikan dengan apps yang sudah ada ?</li>
    <li v-click>Bagaimana jika ada 1000 user akses ke web aplikasi secara bersamaan ?</li>
    <li v-click>Apakah jika ada jutaan data didatabase akan mempengaruhi performance speed load time ?</li>
  </ul>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
