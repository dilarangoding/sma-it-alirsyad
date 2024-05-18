
## Introduction
Tailwind CSS merupakan framework CSS yang berbasis utility untuk membuat UI atau tampilan dari aplikasi web. Dengan menggunakan Tailwind CSS kita dapat membuat tampilan sebuah website dengan cepat.

Equipment: 
1. Visual Studio Code
2. Install Extension Tailwind CSS IntelliSense di VS Code
3. Git ([link](https://git-scm.com/downloads))
4. Asset (Link asset bisa download [disini](https://github.com/dilarangoding/gdsc-studyjam-6))
5. Github ([link](https://github.com/signup))
6. Vercel ([link](https://vercel.com/))
7. Niat yang kuat

## Step 1 - Installation

Ada dua cara yang bisa dilakukan untuk menggunakan Tailwind di dalam project kita yaitu:
1. Menggunakan link CDN
2. Menggunakan NPM dari Node.JS

Pada pertemuan kali ini kita akan menggunakan link CDN. Buat file dengan nama `index.html` dan file `tailwind.config.js` didalam folder `portofolio`, ekstrak file asset yang sudah kita download tadi dan pindahkan ke dalam folder portofolio. Struktur folder nya akan seperti ini.

![[Pasted image 20240518061314.png]]

Buka folder portofolio di Visual Studio Code dan tambahkan kode berikut di dalam file index.html

```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Riyon Aryono</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          container: {
            center: true,
            padding: {
              DEFAULT: 0,
              lg: "135px",
            },
          },
        },
      };
    </script>
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello World</h1>
  </body>
</html>

```

## Step 2 - Builing the Hero Section

Hero section akan berisikan navbar dan juga kita akan mendisplay informasi tentang kita secara singkat dan juga beberapa icon ke sosial media kita.

``` HTML
<!-- Hero -->
    <section class="w-full bg-[#F6C71F] h-screen">
      <div class="flex flex-col container h-full">
        <!-- Navbar -->
        <div class="flex flex-row justify-between pt-[58px]">
          <span class="flex flex-row font-bold">RY</span>
          <img src="img/menu.svg" class="w-[24px] cursor-pointer" />
        </div>
        <!-- End Navbar -->

        <!-- Introduction -->
        <div class="flex grow flex-row">
          <!-- Left Side -->
          <div class="flex flex-col justify-center w-1/2">
            <p class="text-[65px] leading-tight font-medium">
              Hi, I'm Riyon, <br />
              I Develop Stuff,
            </p>
            <p class="text-[14px] mt-[40px]">
              I enjoy listening to Bossa Nova, Psychedelic, and K-Pop music.
              Outside of work, I collect cassette tapes and learning Golang
            </p>

            <div class="inline-flex mt-[40px] space-x-[24px]">
              <button
                class="text-[16px] py-[10px] px-[45px] bg-black rounded-full text-white hover:shadow-lg"
              >
                Let's Work
              </button>
              <button
                class="text-[16px] py-[10px] px-[45px] border-2 border-black rounded-full hover:shadow-lg"
              >
                See my work
              </button>
            </div>

            <div class="inline-flex space-x-[24px] mt-[100px]">
              <img src="img/fb.svg" class="w-[24px]" />
              <img src="img/x.svg" class="w-[24px]" />
              <a href="https://www.instagram.com/riyonaryonoo">
                <img src="img/ig.svg" class="w-[24px]"
              /></a>
              <img src="img/medium.svg" class="w-[24px]" />
            </div>
          </div>
          <!-- Right Side -->
          <div class="grid w-1/2">
            <img src="img/cowo.png" class="w-5/6 place-self-end" />
          </div>
        </div>
        <!-- End Introdcation -->
      </div>
    </section>
    <!-- End Hero -->
```

## Step 3 - Building the Portofolio Section

Distep ini kita akan mendisplay portofolio seperti projek, kegitan atau apapun di section ini.

Tambahkan kode ini dibawah hero section:

```HTML
<!-- Porto -->
    <section class="w-full container mt-[100px]">
      <p class="text-[30px] font-bold">Portofolio</p>
      <p class="">
        I've worked with a couple of innovate brands over the years, here's a
        selection of some my favorite works.
      </p>
      <div class="grid grid-cols-5 items-center gap-[70px] mt-[40px]">
        <img src="img/telkom.png" />
        <img src="img/tokopedia.png" />
        <img src="img/shopee.png" />
        <img src="img/gojek.png" />
      </div>

      <div
        class="inline-flex space-x-[24px] mt-[80px] text-[16px] text-neutral-500"
      >
        <span class="text-neutral-900 font-bold">All Works</span>
        <span>Web Development</span>
        <span>Android Development</span>
        <span>Game Development</span>
        <span>UI & UX</span>
      </div>

      <div class="grid grid-cols-3 gap-[40px] mt-[20px]">
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
      </div>
    </section>
    <!-- End Porto -->
  <div class="border border-neutral-500 w-1/3 container my-[100px]"></div>
```

### Step 4 - Building the Colaborate Section

Step ini kita akan membuat tampilan untuk ajakan berkolaborasi client dengan kita 

tambahkan kode berikut dibawah section portofolio:

```HTML
   <!-- Porto -->
    <section class="w-full container mt-[100px]">
      <p class="text-[30px] font-bold">Portofolio</p>
      <p class="">
        I've worked with a couple of innovate brands over the years, here's a
        selection of some my favorite works.
      </p>
      <div class="grid grid-cols-5 items-center gap-[70px] mt-[40px]">
        <img src="img/telkom.png" />
        <img src="img/tokopedia.png" />
        <img src="img/shopee.png" />
        <img src="img/gojek.png" />
      </div>

      <div
        class="inline-flex space-x-[24px] mt-[80px] text-[16px] text-neutral-500"
      >
        <span class="text-neutral-900 font-bold">All Works</span>
        <span>Web Development</span>
        <span>Android Development</span>
        <span>Game Development</span>
        <span>UI & UX</span>
      </div>

      <div class="grid grid-cols-3 gap-[40px] mt-[20px]">
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
      </div>
    </section>
    <!-- End Porto -->
```

## Step 5 - Building the Footer Section

Ini adalah section terakhir di halaman web kita, disection ini kita akan membuat sebuah footer untuk ekstra link seperti link `about me`, `contact` dan semacamnya

Tambahkan kode berikut dibawah section porto

```HTML
 <!-- Footer -->
    <footer class="border-t bg-zinc-100 mt-[100px]">
      <div class="grid grid-cols-4 container py-[50px]">
        <div class="flex flex-col">
          <div
            class="w-[100px] h-[100px] bg-zinc-200 border-2 border-zinc-300 rounded-lg"
          ></div>
          <div class="inline-flex space-x-[24px] mt-[24px] opacity-50">
            <img src="img/fb.svg" class="w-[20px]" />
            <img src="img/x.svg" class="w-[20px]" />
            <img src="img/ig.svg" class="w-[20px]" />
            <img src="img/medium.svg" class="w-[20px]" />
          </div>
        </div>

        <div class="flex flex-col space-y-4 text-zinc-500">
          <a href="#">About Me</a>
          <a href="#">Contact</a>
          <a href="#">Testimonial</a>
          <a href="#">Reference</a>
        </div>

        <div class="flex flex-col space-y-4 text-zinc-500">
          <a href="#">Portofolio</a>
          <a href="#">Store</a>
          <a href="#">Books</a>
        </div>

        <div class="flex flex-col space-y-4 text-zinc-500">
          <a href="#">Get in touch</a>
          <a href="#" class="mt-[24px] font-semibold text-black">
            +62 8123456789</a
          >
          <a href="#" class="font-semibold text-black">
            riyonaryono@gmail.com</a
          >
        </div>
      </div>
      <p class="py-[12px] text-[14px] text-center text-neutral-500">
        2024 Riyon Aryono. All rights reserved
      </p>
    </footer>
    <!-- End Footer -->
```


Fulll Kode

```HTML

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Riyon Aryono</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
      tailwind.config = {
        theme: {
          container: {
            center: true,
            padding: {
              DEFAULT: 0,
              lg: "135px",
            },
          },
        },
      };
    </script>
  </head>

  <body>
    <!-- Hero -->
    <section class="w-full bg-[#F6C71F] h-screen">
      <div class="flex flex-col container h-full">
        <!-- Navbar -->
        <div class="flex flex-row justify-between pt-[58px]">
          <span class="flex flex-row font-bold">RY</span>
          <img src="img/menu.svg" class="w-[24px] cursor-pointer" />
        </div>
        <!-- End Navbar -->

        <!-- Introduction -->
        <div class="flex grow flex-row">
          <!-- Left Side -->
          <div class="flex flex-col justify-center w-1/2">
            <p class="text-[65px] leading-tight font-medium">
              Hi, I'm Riyon, <br />
              I Develop Stuff,
            </p>
            <p class="text-[14px] mt-[40px]">
              I enjoy listening to Bossa Nova, Psychedelic, and K-Pop music.
              Outside of work, I collect cassette tapes and learning Golang
            </p>

            <div class="inline-flex mt-[40px] space-x-[24px]">
              <button
                class="text-[16px] py-[10px] px-[45px] bg-black rounded-full text-white hover:shadow-lg"
              >
                Let's Work
              </button>
              <button
                class="text-[16px] py-[10px] px-[45px] border-2 border-black rounded-full hover:shadow-lg"
              >
                See my work
              </button>
            </div>

            <div class="inline-flex space-x-[24px] mt-[100px]">
              <img src="img/fb.svg" class="w-[24px]" />
              <img src="img/x.svg" class="w-[24px]" />
              <a href="https://www.instagram.com/riyonaryonoo">
                <img src="img/ig.svg" class="w-[24px]"
              /></a>
              <img src="img/medium.svg" class="w-[24px]" />
            </div>
          </div>
          <!-- Right Side -->
          <div class="grid w-1/2">
            <img src="img/cowo.png" class="w-5/6 place-self-end" />
          </div>
        </div>
        <!-- End Introdcation -->
      </div>
    </section>
    <!-- End Hero -->

    <!-- Porto -->
    <section class="w-full container mt-[100px]">
      <p class="text-[30px] font-bold">Portofolio</p>
      <p class="">
        I've worked with a couple of innovate brands over the years, here's a
        selection of some my favorite works.
      </p>
      <div class="grid grid-cols-5 items-center gap-[70px] mt-[40px]">
        <img src="img/telkom.png" />
        <img src="img/tokopedia.png" />
        <img src="img/shopee.png" />
        <img src="img/gojek.png" />
      </div>

      <div
        class="inline-flex space-x-[24px] mt-[80px] text-[16px] text-neutral-500"
      >
        <span class="text-neutral-900 font-bold">All Works</span>
        <span>Web Development</span>
        <span>Android Development</span>
        <span>Game Development</span>
        <span>UI & UX</span>
      </div>

      <div class="grid grid-cols-3 gap-[40px] mt-[20px]">
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
        <div class="aspect-square bg-zinc-200 rounded-xl"></div>
      </div>
    </section>
    <!-- End Porto -->

    <div class="border border-neutral-500 w-1/3 container my-[100px]"></div>

    <!-- Colaborate -->
    <section class="text-center">
      <p class="text-[42px] font-semibold">Want to collaborate?</p>
      <p class="text-[18px]">
        You can shoot me an email or we could have a quick chat.
      </p>
      <div class="mt-[50px]">
        <button
          class="text-[16px] py-[10px] px-[45px] bg-black rounded-full text-white hover:shadow-lg"
        >
          Get in touch
        </button>
      </div>
    </section>
    <!-- End Colaborate -->

    <!-- Footer -->
    <footer class="border-t bg-zinc-100 mt-[100px]">
      <div class="grid grid-cols-4 container py-[50px]">
        <div class="flex flex-col">
          <div
            class="w-[100px] h-[100px] bg-zinc-200 border-2 border-zinc-300 rounded-lg"
          ></div>
          <div class="inline-flex space-x-[24px] mt-[24px] opacity-50">
            <img src="img/fb.svg" class="w-[20px]" />
            <img src="img/x.svg" class="w-[20px]" />
            <img src="img/ig.svg" class="w-[20px]" />
            <img src="img/medium.svg" class="w-[20px]" />
          </div>
        </div>

        <div class="flex flex-col space-y-4 text-zinc-500">
          <a href="#">About Me</a>
          <a href="#">Contact</a>
          <a href="#">Testimonial</a>
          <a href="#">Reference</a>
        </div>

        <div class="flex flex-col space-y-4 text-zinc-500">
          <a href="#">Portofolio</a>
          <a href="#">Store</a>
          <a href="#">Books</a>
        </div>

        <div class="flex flex-col space-y-4 text-zinc-500">
          <a href="#">Get in touch</a>
          <a href="#" class="mt-[24px] font-semibold text-black">
            +62 8123456789</a
          >
          <a href="#" class="font-semibold text-black">
            riyonaryono@gmail.com</a
          >
        </div>
      </div>
      <p class="py-[12px] text-[14px] text-center text-neutral-500">
        2024 Riyon Aryono. All rights reserved
      </p>
    </footer>
    <!-- End Footer -->
  </body>
</html>

```


