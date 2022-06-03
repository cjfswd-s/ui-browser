<template>
  <div
    class="flex justify-center items-center h-[1080px] w-[1920px]"
    style="background-image: url('/desktop.png')"
  >
    <div class="flex flex-row h-[863px] w-[1536px]">
      <div class="w-[400px] h-full bg-[#F9F9F9] px-[40px] py-[50px]">
        <div class="relative h-full">
          <div class="flex justify-center h-[32px] mt-[12px] mb-[76px]">
            <img
              src="/pixel-perfect/league-of-legends/riot-logo.png"
              alt=""
              height="32px"
              width="112px"
            />
          </div>
          <div class="px-[16px] mb-[24px]">
            <p class="mb-[27px] text-[24px] font-semibold text-center">Sign In</p>
            <div
              class="rounded bg-[#ededed] mb-[16px] px-[16px] py-[18px] text-[8px] leading-[8px] font-semibold text-[#999999]"
            >
              USERNAME
            </div>
            <div
              class="rounded bg-[#ededed] mb-[16px] px-[16px] py-[18px] text-[8px] leading-[8px] font-semibold text-[#999999]"
            >
              PASSWORD
            </div>
            <div class="h-[32px] grid grid-cols-3 gap-[8px] mb-[12px]">
              <div
                class="flex justify-center items-center bg-[#1877f2] full text-white rounded border-2 border-[#1771e6] mdi mdi-facebook"
              ></div>
              <div
                class="flex justify-center items-center bg-white full text-white rounded border-2 border-[#f2f2f2]"
              >
                <img
                  src="https://upload.wikimedia.org/wikipedia/commons/5/53/Google_%22G%22_Logo.svg"
                  width="14px"
                />
              </div>
              <div
                class="flex justify-center items-center bg-[#000000] full text-white rounded border-2 border-[#0d0d0d] mdi mdi-apple"
              ></div>
            </div>
            <div class="flex items-center gap-[8px]">
              <div class="rounded h-[16px] w-[16px] bg-[#e6e6e6]"></div>
              <span class="text-[14px] font-semibold">Stay signed in</span>
            </div>
          </div>
          <div
            class="flex flex-col justify-center items-center text-center w-full absolute bottom-0 left-0 text-[#b2b2b2] text-[8px] font-semibold"
          >
            <div
              class="mb-[60px] flex justify-center items-center h-[64px] w-[64px] rounded-[16px] text-[32px] text-[#e8e8e8] border-2 border-[#e8e8e8] mdi mdi-arrow-right"
            ></div>
            <div>
              <p class="mb-2">CAN'T SIGN IN?</p>
              <p>CREATE ACCOUNT</p>
            </div>
          </div>
          <div class="absolute bottom-0 right-0 text-[#cac7c7] text-[8px] font-semibold">
            V49.0.2
          </div>
        </div>
      </div>
      <div
        class="relative block w-[1137px] h-full"
        style="
          background-image: url('/pixel-perfect/league-of-legends/side-background.jpg');
          background-position: center;
          background-repeat: no-repeat;
          background-size: contain;
        "
      >
        &nbsp;
        <div
          style="transform: rotate(45deg)"
          class="shadow-2xl bg-[#d950e5] flex justify-center items-center rounded h-[50px] w-[50px] absolute flex jusitfy-center items-center gap-[20px] top-[30px] left-[32px] text-black font-semibold leading-none"
        >
          <div
            style="transform: rotate(-45deg)"
            class="text-[32px] mdi mdi-exclamation-thick"
          ></div>
        </div>
        <div
          class="shadow bg-white/10 flex justify-center items-center rounded-[16px] h-[50px] w-[50px] absolute flex jusitfy-center items-center gap-[20px] top-[30px] right-[32px] text-[#bfaea7] font-semibold leading-none"
        >
          <div class="text-[24px] mdi mdi-account"></div>
        </div>
        <div
          class="h-[24px] absolute flex jusitfy-center items-center gap-[20px] mr-[10px] top-0 right-0 text-[#cac7c7] font-semibold leading-none"
        >
          <div
            class="flex jusitfy-center items-end text-[16px] mdi mdi-window-minimize"
          ></div>
          <div class="text-[16px] mdi mdi-window-close"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans&display=swap");

html {
  width: 100%;
  height: 100%;
  font-family: "IBM Plex Sans", sans-serif;
}
</style>
