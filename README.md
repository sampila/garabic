<p align="center" width="100%">
     <img alt="Arabic tools for golang - حزمة أدوات للتعامل مع اللغة العربية في لغة go" src=".github/logo.png"> 
</p>

# ar-golang

[![GoDoc][godoc-image]][godoc-url]
[![codecov][codecov-image]][codecov-url]
[![Build Status][travis-image]][travis-url]

> A set of functions for Arabic text processing in golang

> مكتبة برمجية توفر دوالاً للتعامل مع النصوص العربية في لغة برمجة  go


# Features

* [x] Normalize arabic text for processing.
* [x] Remove Harakat from arabic text.
* [x] Arabic numbers to words.
* [ ] English-Arabic Transliteration.
* [ ] Hijri date support.
* [ ] Arabic Sentiment Analysis.
* [ ] Arabic Glyphs shaping to render arabic text properly in images.
* [ ] Add diacritics to arabic text 

# المزايا

* [x] تنميط الحروف
* [x] اختزال التشكيل
* [x] تحويل الأعداد إلى كلمات
* [ ] دعم قراءة و تحويل النص العربي لحروف انجليزية
* [ ] التاريخ الهجري
* [ ] تحليل المشاعر في النص العربي
* [ ] اصلاح تشبيك النص العربي
* [ ] تشكيل النص العربي

## Usage

The following example prints out matches with the matched chars in bold.

```go
package main

import (
	"fmt"

	arabic "github.com/AbdullahDiaa/ar-golang"
)

func main() {
     normalized := arabic.RemoveHarakat("سَنواتٌ")
	fmt.Println(normalized)
	// Output:
	// سنوات
}
```

# Speed
Here's a benchmark for normalizing ~78K words on MBP i5 takes about ~45ms:
```
BenchmarkNormalizeBigText-4           25          45546613 ns/op         9275097 B/op         31 allocs/op
~45 ms
```

# Documentation

[GoDoc][godoc-url].

# Contributing

Everyone is welcome to contribute. Please send me a pull request or file an issue. I promise to respond promptly.

# License

[Apache License 2.0][licence-url]

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.


[codecov-image]: https://codecov.io/gh/AbdullahDiaa/ar-golang/branch/main/graph/badge.svg?token=2RS36L0KVL
[codecov-url]: https://codecov.io/gh/AbdullahDiaa/ar-golang
[travis-image]: https://travis-ci.com/AbdullahDiaa/ar-golang.svg?token=xpANNwyiLEp99ynBzKhp&branch=main
[travis-url]: https://travis-ci.com/AbdullahDiaa/ar-golang
[godoc-image]: https://godoc.org/github.com/AbdullahDiaa/ar-golang?status.svg
[godoc-url]: https://godoc.org/github.com/AbdullahDiaa/ar-golang
[licence-url]: https://github.com/AbdullahDiaa/ar-golang/blob/main/LICENSE