<template>
  <section id="section-banner" class="site-banner">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 col-md-12 site-title margin-banner-text">
          <div class="ml-md-5 ml-lg-0">
            <h3 class="title-text">{{ $t("Banner.greeting") }}</h3>
            <h1 class="title-text text-uppercase">{{ $t("Banner.title") }}</h1>
            <h4 class="title-text text-uppercase">Full-stack web developer</h4>
          </div>

          <div class="site-button ml-md-5 ml-lg-0">
            <div class="d-flex flex-row flex-wrap">
              <button
                class="btn button primary-button  mr-md-0 mr-lg-4 text-uppercase"
              >
                {{ $t("Banner.btn1") }}
              </button>
              <button
                class="btn button secundary-button  mt-md-0  mr-md-0  mr-lg-4 text-uppercase"
              >
                {{ $t("Banner.btn2") }}
              </button>
            </div>
          </div>

          <!-- <div style="transform: translate(5%) rotate(270deg)">
            <svg class="svg-name" viewBox="0 0 184 100">
              <path
                d="M182 184a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20 0a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20 0a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20 40a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20 60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm-20 80a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zM22 144a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zM2 144a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-60a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0-20a2 2 0 1 1 0-4 2 2 0 0 1 0 4zM2 4a2 2 0 1 1 0-4 2 2 0 0 1 0 4z"
                fill="#4E68D0"
                fill-rule="evenodd"
                opacity=".503"
              />
            </svg>
          </div> -->
        </div>
        <div class="col-lg-6 col-md-12 pl-md-0 pl-lg-5  banner-image">
          <div class="d-flex justify-content-center">
            <svg width="80%" viewBox="0 0 863 826.714">
              <title>undraw_laravel_and_vue_59tp</title>
              <g>
                <path
                  d="M908.585 346.03C863.668 169.408 708.468 41.912 526.296 36.799 429.988 34.095 328.644 66.036 254.86 177.81c-131.9 199.809 8.105 337.883 105.713 403.493a610.758 610.758 0 0 1 126.241 113.465c65.931 78.237 192.767 175.459 343.824 23.128 109.485-110.41 107.866-254.219 77.948-371.866z"
                  transform="translate(-168.5 -36.643)"
                  fill="#f2f2f2"
                ></path>
                <path
                  d="M1030.5 739.357c0 43.354-189.19 124-427.5 124s-434.5-75.646-434.5-119 196.19-38 434.5-38 427.5-10.354 427.5 33z"
                  transform="translate(-168.5 -36.643)"
                  fill="#3f3d56"
                ></path>
                <path
                  d="M1030.5 739.357c0 43.354-189.19 124-427.5 124s-434.5-75.646-434.5-119 196.19-38 434.5-38 427.5-10.354 427.5 33z"
                  transform="translate(-168.5 -36.643)"
                  opacity=".1"
                ></path>
                <ellipse
                  cx="431.5"
                  cy="707.214"
                  rx="431.5"
                  ry="78.5"
                  fill="#3f3d56"
                ></ellipse>
                <path
                  fill="#2f2e41"
                  d="M594.859 440.238v209.944l35.117 57.231 2.673 4.353h138.563l2.799-271.528H594.859z"
                ></path>
                <path
                  opacity=".1"
                  d="M594.859 440.238v209.944l35.117 57.231 2.155-267.175h-37.272z"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M260.348 434.639v209.944l-35.117 57.231-2.673 4.353H83.994l-2.799-271.528h179.153z"
                ></path>
                <path
                  opacity=".1"
                  d="M260.348 434.639v209.944l-35.117 57.231-2.156-267.175h37.273z"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M816 430.44v12.597H63v-18.195l69.981-36.39h621.435L816 430.44z"
                ></path>
                <path
                  opacity=".1"
                  d="M816 430.44v12.597H63v-18.195l753 5.598z"
                ></path>
                <path
                  opacity=".1"
                  d="M170.771 493.424H137.18l-13.996-9.798h62.983l-15.396 9.798z"
                ></path>
                <path
                  opacity=".1"
                  d="M170.771 534.013H137.18l-13.996-9.798h62.983l-15.396 9.798z"
                ></path>
                <path
                  opacity=".1"
                  d="M170.771 591.398H137.18l-13.996-9.798h62.983l-15.396 9.798z"
                ></path>
                <path
                  opacity=".1"
                  d="M170.771 648.782H137.18l-13.996-9.797h62.983l-15.396 9.797z"
                ></path>
                <path
                  opacity=".1"
                  d="M684.435 499.022h33.591l13.996-9.797h-62.983l15.396 9.797z"
                ></path>
                <path
                  opacity=".1"
                  d="M684.435 539.611h33.591l13.996-9.797h-62.983l15.396 9.797z"
                ></path>
                <path
                  opacity=".1"
                  d="M684.435 596.996h33.591l13.996-9.797h-62.983l15.396 9.797z"
                ></path>
                <path
                  opacity=".1"
                  d="M684.435 654.381h33.591l13.996-9.798h-62.983l15.396 9.798z"
                ></path>
                <path
                  d="M701.016 390.07l-4.669 29.807s-22.984 12.21-6.823 12.57 92.295 0 92.295 0 14.724 0-8.619-12.93l-4.668-31.243z"
                  transform="translate(-168.5 -36.643)"
                  fill="#3f3d56"
                ></path>
                <path
                  d="M686.273 432.123a63.569 63.569 0 0 1 10.074-6.669l4.669-29.807 67.516.063 4.668 29.385a61.304 61.304 0 0 1 10.789 7.1c2.998-.685 6.274-3.227-10.789-12.677l-4.669-31.244-67.515 1.796-4.669 29.807s-19.313 10.262-10.074 12.246z"
                  transform="translate(-168.5 -36.643)"
                  opacity=".1"
                ></path>
                <rect
                  x="413.824"
                  y="145.672"
                  width="304.18"
                  height="211.885"
                  rx="10.695"
                  fill="#3f3d56"
                ></rect>
                <path
                  fill="#f2f2f2"
                  d="M424.059 156.984h283.71v158.734h-283.71z"
                ></path>
                <circle
                  cx="565.914"
                  cy="151.957"
                  r="1.796"
                  fill="#f2f2f2"
                ></circle>
                <path
                  d="M886.505 364.93v18.575a10.693 10.693 0 0 1-10.695 10.694H593.02a10.693 10.693 0 0 1-10.696-10.694V364.93z"
                  transform="translate(-168.5 -36.643)"
                  fill="#3f3d56"
                ></path>
                <circle
                  cx="565.914"
                  cy="343.012"
                  r="6.823"
                  fill="#f2f2f2"
                ></circle>
                <path
                  fill="#3f3d56"
                  d="M555.281 415.196v3.592h-193.21v-2.873l.266-.719 4.762-12.928h184.232l3.95 12.928z"
                ></path>
                <path
                  d="M798.135 448.323c-.352 1.505-1.68 3.093-4.683 4.594-10.774 5.387-32.68-1.437-32.68-1.437s-16.88-2.873-16.88-10.415a13.468 13.468 0 0 1 1.48-.88c4.53-2.396 19.548-8.31 46.178.251a11.106 11.106 0 0 1 5.062 3.317 5.296 5.296 0 0 1 1.523 4.57z"
                  transform="translate(-168.5 -36.643)"
                  fill="#3f3d56"
                ></path>
                <path
                  d="M798.135 448.323c-13.187 5.053-24.941 5.43-37.004-2.948-6.084-4.223-11.61-5.268-15.759-5.19 4.53-2.396 19.548-8.31 46.178.251a11.106 11.106 0 0 1 5.062 3.317 5.296 5.296 0 0 1 1.523 4.57z"
                  transform="translate(-168.5 -36.643)"
                  opacity=".1"
                ></path>
                <ellipse
                  cx="613.101"
                  cy="407.296"
                  rx="4.669"
                  ry="1.437"
                  fill="#f2f2f2"
                ></ellipse>
                <path
                  opacity=".1"
                  d="M555.281 415.196v3.592h-193.21v-2.873l.266-.719h192.944z"
                ></path>
                <path
                  d="M834.194 268.594c-1.525-1.524-21.088-26.168-24.39-30.233-3.557-4.065-5.082-3.303-7.368-3.05s-26.931 4.574-29.726 4.828c-2.795.508-4.573 1.524-2.795 4.065 1.525 2.287 17.785 25.152 21.342 30.488L726.47 290.19l-51.321-86.128c-2.033-3.049-2.541-4.065-7.114-3.811s-40.396 3.303-42.937 3.303c-2.54.254-5.335 1.27-2.795 7.368s43.191 93.495 44.207 96.036 4.065 6.605 10.925 5.081c7.114-1.778 31.504-8.13 44.97-11.687 7.113 12.703 21.34 38.618 24.136 42.429 3.556 5.081 6.097 4.065 11.432 2.54 4.32-1.27 66.565-23.628 69.36-24.898s4.573-2.032 2.54-4.827c-1.524-2.033-17.784-24.136-26.422-35.57 5.843-1.523 26.93-7.113 29.217-7.875 2.54-.762 3.049-2.033 1.525-3.557zM716.562 292.73c-.762.254-37.093 8.892-38.872 9.4-2.032.509-2.032.255-2.032-.508-.508-.762-43.191-89.176-43.953-90.192-.509-1.017-.509-2.033 0-2.033s34.298-3.049 35.314-3.049c1.27 0 1.017.255 1.525 1.017 0 0 47.51 82.062 48.272 83.333 1.016 1.27.508 1.778-.254 2.032zm102.134 19.055c.508 1.016 1.27 1.524-.762 2.033-1.779.762-61.23 20.833-62.5 21.34s-2.033.763-3.557-1.523-20.833-35.57-20.833-35.57l63.262-16.514c1.524-.508 2.032-.762 3.048.763 1.017 1.778 20.834 28.709 21.342 29.471zm4.065-44.715c-1.525.254-24.644 6.097-24.644 6.097l-19.055-25.914c-.508-.762-1.017-1.525.254-1.779s22.866-4.065 23.882-4.319 1.778-.508 3.049 1.27c1.27 1.525 17.53 22.358 18.292 23.12s-.254 1.27-1.778 1.525z"
                  transform="translate(-168.5 -36.643)"
                  fill="#fb503b"
                ></path>
                <circle
                  cx="394.639"
                  cy="155.895"
                  r="38.247"
                  fill="#ffb9b9"
                ></circle>
                <path
                  d="M534.957 211.66v60.39h62.403s-8.052-50.324-4.026-65.422z"
                  transform="translate(-168.5 -36.643)"
                  fill="#ffb9b9"
                ></path>
                <path
                  d="M658.756 293.187s-59.383-29.189-59.383-31.202-6.04-15.097-10.065-15.097-38.247-11.071-57.37 5.032l-2.013 13.085-73.474 48.311 20.13 73.474s13.084 14.091 9.058 24.156 3.02 61.396 3.02 61.396l158.019-5.032v-68.442s5.032-16.104 8.052-21.136 0-20.13 0-20.13l24.156-30.195s-3.02-28.182-20.13-34.22z"
                  transform="translate(-168.5 -36.643)"
                  fill="#d0cde1"
                ></path>
                <path
                  d="M458.967 337.975l4.53-24.659s-26.17 113.734-23.15 126.818 25.162 33.215 28.182 34.221 31.201-86.558 31.201-86.558z"
                  transform="translate(-168.5 -36.643)"
                  opacity=".1"
                ></path>
                <path
                  d="M473.561 310.297l-17.11 3.02S430.282 427.05 433.3 440.133s25.163 33.215 28.182 34.221 31.202-86.558 31.202-86.558z"
                  transform="translate(-168.5 -36.643)"
                  fill="#d0cde1"
                ></path>
                <path
                  d="M664.291 344.014l8.556-16.607s12.077 113.734 4.026 124.805-39.903 15.214-39.903 15.214l-.357-82.649z"
                  transform="translate(-168.5 -36.643)"
                  opacity=".1"
                ></path>
                <path
                  d="M665.801 314.323l13.085 13.084s12.077 113.734 4.026 124.805-39.903 15.214-39.903 15.214l-.357-82.649z"
                  transform="translate(-168.5 -36.643)"
                  fill="#d0cde1"
                ></path>
                <path
                  d="M470.542 487.44s-29.188-11.072-34.22 10.064 12.077 115.747 12.077 115.747 11.071 71.46 18.117 73.474 38.247 3.02 43.279-6.04-15.097-101.655-15.097-101.655l116.753-2.013s-7.046 80.52-11.072 87.565-4.026 31.201 0 31.201 48.312-2.013 51.331-8.052 20.13-141.915 20.13-141.915 14.091-47.305-2.013-44.286-199.285-14.09-199.285-14.09z"
                  transform="translate(-168.5 -36.643)"
                  fill="#3f3d56"
                ></path>
                <path
                  d="M642.652 683.705s10.065-7.045 15.097 0 7.046 15.098-15.097 27.175-39.253 9.059-39.253 7.046v-29.188z"
                  transform="translate(-168.5 -36.643)"
                  fill="#2f2e41"
                ></path>
                <path
                  d="M468.529 680.686s-10.065-7.046-15.098 0-7.045 15.097 15.098 27.175 39.253 9.058 39.253 7.045v-29.188z"
                  transform="translate(-168.5 -36.643)"
                  fill="#2f2e41"
                ></path>
                <path
                  d="M563.387 144.312a32.348 32.348 0 0 0-11.233 1.601 43.428 43.428 0 0 0-8.003 4.234l-16.886 10.5a7.908 7.908 0 0 0-4.766 7.37l-2.11 15.802c-.532 3.988-1.023 8.253.762 11.858 1.49 3.01 4.331 5.069 6.668 7.48a27.456 27.456 0 0 1 7.236 14.061c1.208 6.598.435 14.543 5.656 18.753 2.827 2.28 6.68 2.711 10.306 2.923a153.786 153.786 0 0 0 29.7-1.143 11.82 11.82 0 0 0 4.488-1.257c1.775-1.05 2.892-2.904 3.937-4.682 3.77-6.42 7.657-13.249 7.616-20.694-.02-3.683-.963-7.639.806-10.87a42.497 42.497 0 0 1 3.037-3.945c2.19-3.076 2.616-7.03 2.973-10.79 1.14-12.008-.052-21.146-8.902-29.606-8.262-7.896-20.018-11.522-31.285-11.595z"
                  transform="translate(-168.5 -36.643)"
                  fill="#2f2e41"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M300.937 569.703l-33.591 170.755h16.795l32.192-167.955-15.396-2.8z"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M408.708 583.7l20.995 195.948h13.996l-12.597-201.547-22.394 5.599z"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M466.093 578.101l29.392 130.166h13.996l-27.992-132.965-15.396 2.799z"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M354.123 578.101l-4.199 103.573h11.197l8.398-103.573h-15.396z"
                ></path>
                <path
                  d="M445.643 588.151s-22.394-149.76 40.59-153.959 152.559 0 152.559 0 51.786-4.199 36.39 153.96c0 0 13.996 46.187-111.97 41.988S445.643 588.15 445.643 588.15z"
                  transform="translate(-168.5 -36.643)"
                  fill="#854fee"
                ></path>
                <path
                  d="M1019.5 649.308c0 26.115-15.525 35.234-34.676 35.234s-34.677-9.119-34.677-35.234 34.677-59.338 34.677-59.338 34.676 33.223 34.676 59.338z"
                  transform="translate(-168.5 -36.643)"
                  fill="#854fee"
                ></path>
                <path
                  fill="#3f3d56"
                  d="M815.416 622.048l14.779-27.039-14.724 23.61.16-9.827 10.186-19.563-10.144 16.962.287-17.675 10.908-15.574-10.863 12.795.18-32.41-1.079 41.067-11.046-16.907 10.912 20.372-1.033 19.74-.031-.524-12.785-17.863 12.746 19.714-.129 2.469-.023.037.011.203-2.622 26.342h3.503l.42-2.128 12.715-19.667-12.684 17.722.356-21.856z"
                ></path>
                <path
                  fill="#2f2e41"
                  d="M838.47 704.549h-41.341l-10.684-60.386h60.386l-8.361 60.386z"
                ></path>
                <path fill="#3f3d56" d="M145 296.3h86v100.828h-86z"></path>
                <path
                  fill="#f2f2f2"
                  d="M158.345 311.946h59.31v69.536h-59.31z"
                ></path>
                <path
                  d="M362.444 363.357l-6.023 10.432-6.023-10.432h-20.055l26.078 45.17 26.079-45.17z"
                  transform="translate(-168.5 -36.643)"
                  fill="#4dba87"
                ></path>
                <path
                  d="M362.444 363.357l-6.023 10.432-6.023-10.432h-9.624l15.647 27.101 15.647-27.1z"
                  transform="translate(-168.5 -36.643)"
                  fill="#435466"
                ></path>
              </g>
            </svg>
          </div>
          <!-- <img src="" alt=""> -->
        </div>
        <div class="box">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.site-main .site-banner .site-title h3 {
  padding-top: 25%;
  font-weight: 500;
}

.site-main .site-banner .site-title h3::after {
  content: "";
  height: 3px;
  width: 22vw;
  background: var(--text-color) !important;
  display: inline-block;
  margin-left: 5%;
  transform: translateY(-10px);
}
.site-main .site-banner .site-title h1 {
  font-size: 5rem;
}

.site-main .site-banner .site-title h4 {
  font-size: 2rem;
}

.site-main .banner-image {
  padding: 4rem 0;
  width: 90rem;
}

.title-text {
  /* font: normal bold 50px/72px var(--roboto); */
  font: normal bold 60px/72px var(--roboto);
  color: var(--text-color);
}

.button {
  padding: 0.8rem 2.2rem;
  font: normal 500 16px/20px var(--roboto);
  position: relative;
  border: 3px solid transparent;
  border-radius: 4px;
  /* color: #fff !important; */
}
.primary-button {
  background: var(--gradient-color);
  background-clip: padding-box;
  /* color: var(--text-color); */
  color: #fff;
  transition: background 0.6s ease;
  box-shadow: var(--box-shadow);
}
.secundary-button {
  background: whitesmoke;
  background-clip: padding-box;
  color: black;
}
.button.primary-button::after,
.button.secundary-button::after {
  position: absolute;
  top: -2px;
  left: -2px;
  bottom: -2px;
  right: -2px;
  background: var(--gradient-color);
  content: "";
  z-index: -1;
  border-radius: 4px;
}
.button.secundary-button {
  background: white;
  background-clip: padding-box;
  transition: background 0.6s ease;
}
.button.secundary-button:hover {
  background: var(--gradient-color);
  color: whitesmoke;
  box-shadow: var(--box-shadow);
}
.button.primary-button:hover {
  color: #fff;
  font-weight: 600;
  box-shadow: 0px 30px 30px rgba(57, 56, 61, 0.205);
  /* letter-spacing: 2px; */
  /* font: normal 600 18px/20px var(--roboto); */
}
.site-main .site-banner .site-title h3 {
  padding-top: 25%;
  font-weight: 500;
}
/* scroll indicator */
.box {
  position: absolute;
  top: 90%;
  left: 47%;
  transform: translate(-50%, -50%);
}
.box span {
  display: block;
  width: 30px;
  height: 30px;
  border-bottom: 3px solid var(--text-color);
  border-right: 3px solid var(--text-color);
  transform: rotate(45deg);
  margin: -5px;
  animation: animate 2s infinite;
}
.box span:nth-child(1) {
  animation-delay: -0.2s;
}
.box span:nth-child(2) {
  animation-delay: -0.4s;
}
@keyframes animate {
  0% {
    opacity: 0;
    transform: rotate(45deg) translate(-20px, -20px);
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: rotate(45deg) translate(20px, 20px);
  }
}
@media only screen and (max-width: 1350px) {
  .box {
    display: none;
  }
}

/* change mobile style */
@media only screen and (max-width: 576px) {
  .margin-banner-text {
    margin: 0 5%;
  }
  .margin-banner-text h1 {
    font-size: 3rem !important;
  }
  .margin-banner-text h4 {
    font-size: 1.2rem !important;
  }
}

@media only screen and (max-width: 400px) {
  .site-main .site-banner .site-title h3::after {
    width: 40vw;
  }
}
</style>
