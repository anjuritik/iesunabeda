<style>
.pattern {
	background: linear-gradient(120deg, #10b981, #6366f1, #10b981, #6366f1, #10b981);
	/* background-image: url('./static/bg-header.svg'); */
}
.try {
	color: white;
	background-color: #0670f4;
	background-image: url(/static/ellipses.svg);
	background-position: 0 50%;
	background-size: cover;
	box-shadow: 0 10px 62px 0 rgb(8 116 249 / 50%);
}
.frosted {
	backdrop-filter: blur(12px);
	background-color: hsla(0, 0%, 100%, 0.6);
}
.frosted-btn {
	backdrop-filter: blur(12px);
	background-color: hsla(0, 0%, 100%, 0.7);
}
.yellow {
	background-color: #fdc700;
}
</style>

<script>
function getLoginUrl() {
	return `https://admin.misiki.in/otplogin`
}
</script>

<div class="container mx-auto max-w-7xl px-4 sm:px-10">
	<div
		class="
        lg:flex lg:items-center lg:justify-between
        p-6
        md:p-10
        lg:p-12
        try
        rounded-lg
      ">
		<h2 class="text-center lg:text-left lg:w-2/5 xl:w-1/2">
			<div class="text-2xl font-semibold">Local Centre Sunabeda Invites you </div>
			<div class="text-xl text-gray-200 mt-3">Join Now</div>
		</h2>

		<div
			class="
          mt-5
          lg:mt-0
          flex flex-wrap
          items-center
          justify-center
          lg:justify-end lg:w-3/5
          xl:w-1/2
          lg:space-x-5
          whitespace-nowrap
          font-semibold
        ">
		</div>
	</div>
</div>
