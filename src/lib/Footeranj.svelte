<style>
.mw-600 {
	max-width: 400px;
}
.purple {
	background-color: #3309f0;
}
.deeppurple {
	background-color: #3309f0;
}
.sub {
	background-color: #3309f0;
}
.connect {
	color: #fddf00;
	font-size: 20px;
	line-height: 29px;
	font-weight: 600;
}
.pro {
	text-align: left;
	color: #fddf00;
}
.form {
	color: #9385be;
}
.form:hover {
	color: white;
}
.reserved {
	color: rgba(121, 105, 165, 0.43);
}

.btn {
	display: block;
	background-image: url(/right-shadow.svg), url(/right-chevron.svg);
	background-position: 107% 100%, 90% 50%;
	background-size: auto 140%, 6px 740px;
	background-repeat: no-repeat, no-repeat;
	background-attachment: scroll, scroll;
}
.btn:hover {
	@apply -translate-y-1;
}
.btn-blue {
	box-shadow: 1px 1px 3px 0 rgba(8, 116, 249, 0.4);
	@apply px-12 font-bold text-white uppercase transition duration-500 ease-in-out transform bg-blue-600 rounded-full;
}
.btn-blue:hover {
	@apply bg-blue-500;
}
.margin {
	margin-right: -1px;
	margin-bottom: -1.5px;
}
</style>

<script>
const d = new Date()
const year = d.getFullYear()
let formData, email

function encode(data) {
	Object.keys(data)
		.map((key) => encodeURIComponent(key) + '=' + encodeURIComponent(data[key]))
		.join('&')
}
function goto() {}

function handleSubmit(e) {
	fetch('https://automation.litekart.in/api/email/subscribe', {
		method: 'POST',
		headers: { 'Content-Type': 'application/json' },
		body: JSON.stringify({
			'form-name': e.target.getAttribute('name'),
			...formData,
		}),
	})
		.then(() => goto('/success'))
		.catch((error) => alert(error))
}
</script>

<section class="items-end mt-12 lg:flex">
	<nav class="relative flex flex-wrap items-center justify-between px-2 py-3  bg-blue-900 mb-1 w-full">
  <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
    <div class="w-full relative flex justify-between lg:w-auto  px-4 lg:static lg:block lg:justify-start">
      <a class="text-sm font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap  text-white" 
      href="#pablo">
     <u>   Our Vision </u>
      </a>
      <button class="cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none" type="button">
        <span class="block relative w-6 h-px rounded-sm bg-white"></span>
        <span class="block relative w-6 h-px rounded-sm bg-white mt-1"></span>
        <span class="block relative w-6 h-px rounded-sm bg-white mt-1"></span>
      </button>
    </div>
    <div class="lg:flex flex-grow items-center" id="example-navbar-warning">
      <ul class="flex flex-col lg:flex-row list-none mr-auto">
        <li class="nav-item">
          <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug text-white hover:opacity-75" href="#pablo">
            <i class="fab fa-facebook-square text-lg leading-lg text-white opacity-75" /> 
          </a>
        </li>
        <li class="nav-item">
          <a class="px-3 py-2 flex items-center text-xs  font-bold leading-snug text-white hover:opacity-75" href="#pablo">
            <i class="fab fa-twitter text-lg leading-lg text-white opacity-75" /> <span class="ml-2">
              <u>Our Work Force</u></span>
          </a>
        </li>
        <li class="nav-item">
          <a class="px-3 py-2 flex items-center text-xs font-bold leading-snug text-white hover:opacity-75" href="#pablo">
            <span class="ml-2"><u>Handout</u></span>
          </a>
        </li>
      </ul>
      <div class="relative flex w-full sm:w-7/12 md:w-5/12 px-4 flex-wrap items-stretch lg:ml-auto">
        <div class="flex">
          <span class="font-normal leading-snug flex text-center white-space-no-wrap border border-solid border-pink-600 rounded-full text-sm bg-pink-100 items-center rounded-r-none pl-2 py-1 text-pink-800 border-r-0 placeholder-pink-300">
            <i class="fas fa-search"></i>
          </span>
        </div>
        <input type="text" class="px-2 py-1 h-8 border border-solid  border-pink-600 rounded-full text-sm leading-snug text-pink-700 bg-pink-100 shadow-none outline-none focus:outline-none w-full font-normal rounded-l-none flex-1 border-l-0 placeholder-pink-300" placeholder="Suggestion" />
      </div>
    </div>
  </div>
</nav>
</section>
