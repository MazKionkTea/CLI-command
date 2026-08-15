| Command | Deskripsi | Contoh |
|---|---|---|
| `# Teks` | Heading tingkat 1 | `# Judul` |
| `## Teks` | Heading tingkat 2 | `## Subjudul` |
| `### Teks` | Heading tingkat 3 | `### Bagian` |
| `#### Teks` | Heading tingkat 4 | `#### Subbagian` |
| `##### Teks` | Heading tingkat 5 | `##### Detail` |
| `###### Teks` | Heading tingkat 6 | `###### Catatan` |
| `**teks**` | Menebalkan teks (bold) | `**Penting**` |
| `__teks__` | Menebalkan teks (alternatif) | `__Penting__` |
| `*teks*` | Memiringkan teks (italic) | `*Catatan*` |
| `_teks_` | Memiringkan teks (alternatif) | `_Catatan_` |
| `***teks***` | Bold dan italic sekaligus | `***Penting***` |
| `___teks___` | Bold dan italic (alternatif) | `___Penting___` |
| `**_teks_**` | Bold + italic dengan kombinasi sintaks | `**_Penting_**` |
| `__*teks*__` | Bold + italic dengan kombinasi alternatif | `__*Penting*__` |
| `~~teks~~` | Mencoret teks (strikethrough) | `~~Salah~~` |
| `` `teks` `` | Inline code | `` `print()` `` |
| ```` ``` ```` | Membuat blok kode | ```` ```\ncode\n``` ```` |
| ```` ```bahasa ```` | Blok kode dengan syntax highlighting | ```` ```python\nprint("Hello")\n``` ```` |
| `> teks` | Blockquote/kutipan | `> Ini adalah kutipan.` |
| `>> teks` | Blockquote bertingkat, jika didukung renderer | `>> Kutipan kedua` |
| `- item` | Unordered list dengan bullet | `- Apel` |
| `* item` | Unordered list alternatif | `* Apel` |
| `+ item` | Unordered list alternatif | `+ Apel` |
| `1. item` | Ordered list bernomor | `1. Pertama` |
| `2. item` | Item berikutnya pada ordered list | `2. Kedua` |
| `1) item` | Ordered list dengan tanda kurung, jika didukung | `1) Pertama` |
| `- [ ] tugas` | Task list/checkbox belum selesai | `- [ ] Belajar Markdown` |
| `- [x] tugas` | Task list/checkbox selesai | `- [x] Belajar Markdown` |
| `- [X] tugas` | Checkbox selesai dengan huruf X kapital | `- [X] Selesai` |
| `  - item` | Nested unordered list | `- Buah\n  - Apel` |
| `  * item` | Nested unordered list alternatif | `* Buah\n  * Apel` |
| `  1. item` | Nested ordered list | `1. Buah\n   1. Apel` |
| `1. item\n   - item` | Nested list dengan tipe berbeda | `1. Buah\n   - Apel` |
| `---` | Horizontal rule/pemisah horizontal | `---` |
| `***` | Horizontal rule alternatif | `***` |
| `___` | Horizontal rule alternatif | `___` |
| `[teks](URL)` | Membuat hyperlink | `[Google](https://google.com)` |
| `[teks](URL "judul")` | Hyperlink dengan title/tooltip | `[Google](https://google.com "Buka Google")` |
| `<URL>` | Automatic link/autolink | `<https://example.com>` |
| `<email>` | Automatic email link | `<user@example.com>` |
| `mailto:email` | Link ke alamat email | `[Email](mailto:user@example.com)` |
| `![alt](URL)` | Menampilkan gambar | `![Logo](https://example.com/logo.png)` |
| `![alt](URL "judul")` | Gambar dengan title/tooltip | `![Logo](image.png "Logo")` |
| `[teks][id]` | Reference-style link | `[Dokumentasi][docs]` |
| `[id]: URL` | Mendefinisikan reference link | `[docs]: https://example.com` |
| `[id]: URL "judul"` | Reference link dengan title | `[docs]: https://example.com "Dokumentasi"` |
| `[id]: URL 'judul'` | Reference link dengan title alternatif | `[docs]: https://example.com 'Dokumentasi'` |
| `[id]: URL (judul)` | Reference link dengan title alternatif | `[docs]: https://example.com (Dokumentasi)` |
| `![alt][id]` | Reference-style image | `![Logo][img]` |
| `[id]: image-url` | Mendefinisikan reference image | `[img]: https://example.com/logo.png` |
| `![alt][id]` + `[id]: URL "title"` | Reference image dengan title | `![Logo][img]` |
| `[teks][]` | Collapsed reference link | `[Dokumentasi][]` |
| `[teks]: URL` | Definisi collapsed reference | `[Dokumentasi]: https://example.com` |
| `[id]` | Shortcut reference link | `[docs]` |
| `[docs]: URL` | Definisi shortcut reference | `[docs]: https://example.com` |
| `\*` | Escape karakter asterisk | `\*teks biasa\*` |
| `\_` | Escape underscore | `\_teks biasa\_` |
| `\#` | Escape hash agar tidak menjadi heading | `\# Bukan heading` |
| `\>` | Escape blockquote | `\> Bukan kutipan` |
| `\-` | Escape tanda minus | `\- Bukan list` |
| `\+` | Escape tanda plus | `\+ Bukan list` |
| `\.` | Escape titik | `1\. Bukan ordered list` |
| `\[` | Escape kurung siku | `\[teks\]` |
| `\]` | Escape kurung siku penutup | `\[teks\]` |
| `\(` | Escape kurung buka | `\(teks\)` |
| `\)` | Escape kurung tutup | `\(teks\)` |
| `\!` | Escape tanda seru | `\!teks` |
| `\\` | Escape backslash | `\\` |
| `\|` | Escape pipe, terutama dalam tabel | `A \| B` |
| `` \` `` | Escape backtick | `` \`kode\` `` |
| `\{` | Escape kurung kurawal | `\{teks\}` |
| `\}` | Escape kurung kurawal penutup | `\{teks\}` |
| `\=` | Escape tanda sama dengan jika diperlukan | `\=teks` |
| `\~` | Escape tilde | `\~teks\~` |
| `\` + punctuation | Escape karakter punctuation Markdown | `\*`, `\_`, `\#`, `\+`, `\-` |
| `` `\` `` | Menampilkan backslash secara literal melalui code span | `` `\` `` |
| `` `` `code` `` `` | Code span dengan double backtick | `` `` `code` `` `` |
| `` ``` `code` ``` `` | Code span dengan triple backtick | `` ``` `code` ``` `` |
| `| Kolom | Kolom |` | Membuat header tabel | `| Nama | Umur |` |
| `|---|---|` | Separator tabel | `|---|---|` |
| `| Data | Data |` | Baris data tabel | `| Budi | 20 |` |
| `|:---|` | Rata kiri pada kolom tabel | `|:---|` |
| `|---:|` | Rata kanan pada kolom tabel | `|---:|` |
| `|:---:|` | Rata tengah pada kolom tabel | `|:---:|` |
| `| A \| B |` | Menampilkan pipe di dalam sel tabel | `| A \| B |` |
| `\|---\|---\|` | Separator tabel dengan karakter pipe yang di-escape dalam konteks tertentu | `\|---\|---\|` |
| `Teks\n\nTeks` | Memisahkan paragraf | `Paragraf 1.\n\nParagraf 2.` |
| `Teks  \nTeks` | Line break dengan dua spasi di akhir baris | `Baris 1  \nBaris 2` |
| `Teks\\\nTeks` | Hard line break menggunakan backslash, jika didukung | `Baris 1\\\nBaris 2` |
| `<br>` | Line break menggunakan HTML | `Baris 1<br>Baris 2` |
| `<br/>` | Line break XHTML-style | `Baris 1<br/>Baris 2` |
| `<!-- komentar -->` | Komentar HTML yang tidak ditampilkan | `<!-- Catatan internal -->` |
| `<!--\nkomentar\n-->` | Komentar HTML multi-baris | `<!--\nCatatan\n-->` |
| `[^1]` | Referensi footnote | `Teks[^1]` |
| `[^1]: teks` | Definisi footnote | `[^1]: Sumber informasi.` |
| `[^1]: teks\n    lanjutan` | Footnote multi-baris | `[^1]: Catatan\n    lanjutan.` |
| `[^nama]` | Footnote dengan identifier teks | `Teks[^sumber]` |
| `[^sumber]: teks` | Definisi named footnote | `[^sumber]: Dokumentasi.` |
| `\n` | Newline dalam representasi Markdown mentah | `Baris 1\nBaris 2` |
| `\n\n` | Pemisah paragraf dalam representasi Markdown mentah | `Paragraf 1\n\nParagraf 2` |
| `&lt;` | Menampilkan karakter `<` menggunakan HTML entity | `&lt;tag&gt;` |
| `&gt;` | Menampilkan karakter `>` menggunakan HTML entity | `&gt;` |
| `&amp;` | Menampilkan karakter `&` | `A &amp; B` |
| `&quot;` | Menampilkan tanda kutip ganda | `&quot;teks&quot;` |
| `&apos;` | Menampilkan apostrof | `&apos;teks&apos;` |
| `&nbsp;` | Non-breaking space | `Nama&nbsp;Lengkap` |
| `&copy;` | Simbol copyright | `&copy; 2026` |
| `&reg;` | Simbol registered trademark | `Brand&reg;` |
| `&trade;` | Simbol trademark | `Brand&trade;` |
| `<details>` | Membuat bagian yang dapat dibuka/tutup, jika HTML didukung | `<details>...</details>` |
| `<summary>` | Menentukan judul elemen `<details>` | `<summary>Detail</summary>` |
| `<details open>` | Membuat `<details>` terbuka secara default | `<details open>...</details>` |
| `<kbd>` | Menampilkan input/tombol keyboard melalui HTML | `<kbd>Ctrl</kbd> + <kbd>C</kbd>` |
| `<mark>` | Menyorot teks melalui HTML | `<mark>Penting</mark>` |
| `<u>` | Underline melalui HTML | `<u>Teks</u>` |
| `<s>` | Strikethrough melalui HTML | `<s>Teks</s>` |
| `<del>` | Menandai teks terhapus melalui HTML | `<del>Teks</del>` |
| `<ins>` | Menandai teks ditambahkan melalui HTML | `<ins>Teks baru</ins>` |
| `<sub>` | Subscript | `H<sub>2</sub>O` |
| `<sup>` | Superscript | `x<sup>2</sup>` |
| `<small>` | Teks berukuran lebih kecil melalui HTML | `<small>Catatan</small>` |
| `<big>` | Teks berukuran lebih besar, jika didukung | `<big>Teks</big>` |
| `<center>` | Meratakan konten ke tengah melalui HTML lama | `<center>Judul</center>` |
| `<div>` | Container HTML untuk konten | `<div>Konten</div>` |
| `<span>` | Container inline HTML | `<span>Teks</span>` |
| `<p>` | Paragraf HTML | `<p>Paragraf.</p>` |
| `<hr>` | Garis horizontal HTML | `<hr>` |
| `<h1>` | Heading HTML tingkat 1 | `<h1>Judul</h1>` |
| `<h2>` | Heading HTML tingkat 2 | `<h2>Subjudul</h2>` |
| `<h3>` | Heading HTML tingkat 3 | `<h3>Bagian</h3>` |
| `<table>` | Membuat tabel menggunakan HTML | `<table>...</table>` |
| `<tr>` | Baris tabel HTML | `<tr>...</tr>` |
| `<th>` | Header tabel HTML | `<th>Nama</th>` |
| `<td>` | Sel tabel HTML | `<td>Budi</td>` |
| `<thead>` | Bagian header tabel HTML | `<thead>...</thead>` |
| `<tbody>` | Bagian isi tabel HTML | `<tbody>...</tbody>` |
| `<tfoot>` | Bagian footer tabel HTML | `<tfoot>...</tfoot>` |
| `<ol>` | Ordered list HTML | `<ol><li>Satu</li></ol>` |
| `<ul>` | Unordered list HTML | `<ul><li>Apel</li></ul>` |
| `<li>` | Item list HTML | `<li>Apel</li>` |
| `<dl>` | Description list HTML | `<dl>...</dl>` |
| `<dt>` | Term pada description list | `<dt>Markdown</dt>` |
| `<dd>` | Deskripsi pada description list | `<dd>Bahasa markup.</dd>` |
| `<blockquote>` | Blockquote HTML | `<blockquote>Kutipan</blockquote>` |
| `<pre>` | Preformatted text HTML | `<pre>teks</pre>` |
| `<code>` | Inline/code HTML | `<code>print()</code>` |
| `<pre><code>` | Code block HTML | `<pre><code>print()</code></pre>` |
| `<a href="URL">teks</a>` | Hyperlink HTML | `<a href="https://example.com">Example</a>` |
| `<img src="URL" alt="teks">` | Gambar HTML | `<img src="image.png" alt="Logo">` |
| `<a href="URL"><img ...></a>` | Gambar yang menjadi hyperlink | `<a href="https://example.com"><img src="logo.png" alt="Logo"></a>` |
| `<details><summary>...</summary>...</details>` | Collapsible section lengkap | `<details><summary>Klik</summary>Isi</details>` |
| `~~teks~~` | Strikethrough GFM | `~~Tidak berlaku~~` |
| `- [ ]` | Task list GFM | `- [ ] Belum` |
| `- [x]` | Completed task GFM | `- [x] Selesai` |
| `| A | B |` | Tabel GFM | `| Nama | Nilai |` |
| `|---|---|` | Separator tabel GFM | `|---|---|` |
| `|:---|---:|` | Alignment kiri dan kanan GFM | `|:---|---:|` |
| `www.example.com` | Bare URL autolink, jika didukung renderer | `www.example.com` |
| `https://example.com` | Bare URL, jika renderer mendukung autolinking | `https://example.com` |
| `user@example.com` | Bare email autolink, jika didukung | `user@example.com` |
| `~~**teks**~~` | Kombinasi strikethrough + bold | `~~**Salah**~~` |
| `***~~teks~~***` | Kombinasi bold, italic, dan strikethrough | `***~~Salah~~***` |
| `**[teks](URL)**` | Bold pada hyperlink | `**[Google](https://google.com)**` |
| `*[teks](URL)*` | Italic pada hyperlink | `*[Google](https://google.com)*` |
| `![alt](URL)` | Gambar Markdown standar | `![Foto](foto.jpg)` |
| `![alt](URL "title")` | Gambar dengan title | `![Foto](foto.jpg "Foto profil")` |
| `[![alt](image)](URL)` | Gambar yang dapat diklik | `[![Logo](logo.png)](https://example.com)` |
| `# Heading #` | ATX heading dengan closing sequence | `# Judul #` |
| `## Heading ##` | ATX heading tingkat 2 dengan closing sequence | `## Subjudul ##` |
| `Heading\n=======` | Setext heading tingkat 1 | `Judul\n=======` |
| `Heading\n-------` | Setext heading tingkat 2 | `Subjudul\n--------` |
| `    kode` | Indented code block | `    print("Hello")` |
| `\t kode` | Indented code block menggunakan tab | `\tprint("Hello")` |
| `---` | Thematic break | `---` |
| `___` | Thematic break | `___` |
| `***` | Thematic break | `***` |
| `- - -` | Thematic break dengan spasi | `- - -` |
| `* * *` | Thematic break dengan spasi | `* * *` |
| `_ _ _` | Thematic break dengan spasi | `_ _ _` |
| `> > teks` | Nested blockquote | `> > Kutipan bertingkat` |
| `> - item` | List di dalam blockquote | `> - Item` |
| `> **teks**` | Formatting di dalam blockquote | `> **Penting**` |
| `> ```code``` ` | Code block di dalam blockquote, jika didukung | `> \`\`\`\ncode\n\`\`\`` |
| `1. item\n2. item` | Ordered list eksplisit | `1. Satu\n2. Dua` |
| `1. item\n1. item` | Ordered list dengan nomor otomatis | `1. Satu\n1. Dua` |
| `1. item\n3. item` | Ordered list dengan nomor awal/urutan eksplisit | `1. Satu\n3. Tiga` |
| `4. item` | Memulai ordered list dari angka tertentu | `4. Empat` |
| `- item\n\n  paragraf` | Paragraf yang masih menjadi bagian list item | `- Item\n\n  Deskripsi item.` |
| `- item\n  ```code``` ` | Code block di dalam list item | `- Item\n\n  \`\`\`\n  code\n  \`\`\`` |
| `[link](<URL dengan spasi>)` | Link destination dengan spasi yang diapit angle brackets | `[Link](<https://example.com/a b>)` |
| `<https://example.com/a_b>` | Autolink URL literal | `<https://example.com/a_b>` |
| `<user+tag@example.com>` | Autolink email | `<user+tag@example.com>` |
| `[teks](URL#anchor)` | Link ke anchor/heading tertentu | `[Bagian](#bagian)` |
| `# Judul {#id}` | Custom heading ID, jika renderer mendukung | `# Judul {#bagian}` |
| `<a id="bagian"></a>` | Membuat anchor HTML manual | `<a id="bagian"></a>` |
| `[Ke bagian](#bagian)` | Link menuju anchor | `[Ke bagian](#bagian)` |
| `[^1]` | Footnote reference | `Informasi[^1]` |
| `[^1]:` | Awal definisi footnote | `[^1]: Penjelasan.` |
| `^[teks]` | Inline footnote, jika renderer mendukung | `Catatan^[Ini catatan inline.]` |
| `==teks==` | Highlight/mark, hanya pada Markdown tertentu | `==Penting==` |
| `++teks++` | Insert/underline extension, jika didukung | `++Teks baru++` |
| `~teks~` | Subscript extension, jika didukung | `H~2~O` |
| `^teks^` | Superscript extension, jika didukung | `x^2^` |
| `::: nama` | Container/directive extension pada renderer tertentu | `::: warning\nPeringatan\n:::` |
| `:::warning` | Admonition/container extension | `:::warning\nHati-hati!\n:::` |
| `> [!NOTE]` | GitHub-style alert NOTE | `> [!NOTE]\n> Informasi.` |
| `> [!TIP]` | GitHub-style alert TIP | `> [!TIP]\n> Tips.` |
| `> [!IMPORTANT]` | GitHub-style alert IMPORTANT | `> [!IMPORTANT]\n> Penting.` |
| `> [!WARNING]` | GitHub-style alert WARNING | `> [!WARNING]\n> Peringatan.` |
| `> [!CAUTION]` | GitHub-style alert CAUTION | `> [!CAUTION]\n> Hati-hati.` |
| `~~~` | Fenced code block alternatif menggunakan tilde | `~~~\ncode\n~~~` |
| `~~~python` | Fenced code block dengan language identifier | `~~~python\nprint("Hello")\n~~~` |
| ```` ```javascript ```` | Syntax highlighting JavaScript | ```` ```javascript\nconsole.log("Hello");\n``` ```` |
| ```` ```json ```` | Syntax highlighting JSON | ```` ```json\n{"key":"value"}\n``` ```` |
| ```` ```html ```` | Syntax highlighting HTML | ```` ```html\n<h1>Hello</h1>\n``` ```` |
| ```` ```css ```` | Syntax highlighting CSS | ```` ```css\nbody { color: red; }\n``` ```` |
| ```` ```bash ```` | Syntax highlighting Bash | ```` ```bash\necho "Hello"\n``` ```` |
| ```` ```sql ```` | Syntax highlighting SQL | ```` ```sql\nSELECT * FROM users;\n``` ```` |
| ```` ```text ```` | Code block tanpa syntax khusus | ```` ```text\nTeks biasa\n``` ```` |
| `<!-- markdown -->` | Menyisipkan HTML yang dapat digunakan bersama Markdown, tergantung sanitizer | `<!-- komentar -->` |
| `<details markdown="1">` | Details dengan atribut Markdown pada renderer tertentu | `<details markdown="1">...</details>` |
| `<table><tr>...</tr></table>` | Tabel HTML untuk layout/fitur yang tidak tersedia pada Markdown standar | `<table><tr><td>A</td></tr></table>` |
| `<img width="...">` | Mengatur lebar gambar dengan HTML | `<img src="foto.png" width="300">` |
| `<img height="...">` | Mengatur tinggi gambar dengan HTML | `<img src="foto.png" height="200">` |
| `<div align="center">` | Meratakan konten ke tengah pada renderer yang mengizinkan HTML | `<div align="center">Tengah</div>` |
| `<p align="center">` | Meratakan paragraf ke tengah menggunakan HTML | `<p align="center">Tengah</p>` |
| `<details open>` | Details terbuka secara default | `<details open><summary>Detail</summary>Isi</details>` |
