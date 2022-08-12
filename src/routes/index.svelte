<script>
	let isError = false;

	let email = '';

	let emailRegex = '/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/';


	const handleClick = () => {
		if (email === emailRegex) {
			console.log('tes');
			isError = false;
		} else {
			isError = true
		}
	};

	$: console.log(email)
</script>

<header>
	<nav class="navbar">
		<div>
			<img src="images/logo.svg" alt="" />
		</div>
		<div class="menus">
			<ul>
				<li class="headerList"><a href="#">Features</a></li>
				<li class="headerList"><a href="#">Team</a></li>
				<li class="headerList"><a href="#">Sign In</a></li>
			</ul>
		</div>
	</nav>
</header>
<div class="topContainer">
	<img src="images/illustration-intro.png" alt="" />
	<div class="topContent">
		<h1 class="topHeader">All your files in one secure location, accessible anywhere.</h1>
		<p class="topSubtitle">
			Fylo stores your most important files in one secure location. Access them wherever you need,
			share and collaborate with friends, family, and co-workers.
		</p>
		<button class="btn">Get Started</button>
	</div>
</div>
<div class="middleContainer">
	<div class="middleImg">
		<div class="middleImgContent">
			<div class="imgContent">
				<img src="images/icon-access-anywhere.svg" alt="" />
				<h1 class="imgHeader">Acces your files, anywhere</h1>
				<p class="imgTxt">
					The ability to use a smartphone, tablet, or computer to access your account means your
					files follow you everywhere
				</p>
			</div>
			<div class="imgContent">
				<img src="images/icon-security.svg" alt="" />
				<h1 class="imgHeader">Security you can trust</h1>
				<p>
					2-factor authentication and user-controlled encryption are just a couple of the security
					features we allow to help secure your files.
				</p>
			</div>
		</div>
		<div class="middleImgContent">
			<div class="imgContent">
				<img src="images/icon-collaboration.svg" alt="" />
				<h1 class="imgHeader">Real-time collaboration</h1>
				<p class="imgTxt">
					Securely share files and folders with friends, famil and colleagues for live
					collaboration. No email attachments required.
				</p>
			</div>
			<div class="imgContent">
				<img src="images/icon-any-file.svg" alt="" />
				<h1 class="imgHeader">Store any type of files</h1>
				<p>
					Whether your're sharing holidays photos or work documents. Fylo has you covered allowing
					for all file types to be securely stored and shared.
				</p>
			</div>
		</div>
		<div class="middleImgTwo">
			<img src="images/illustration-stay-productive.png" alt="" />
			<div class="twoContent">
				<h1 class="twoHeader">Stay productive, wherever you are</h1>
				<p class="twoTxt">
					Never let location be an issue when accessing your files. Fylo has you covered for all of
					your file storage needs.
				</p>
				<p class="twoTxt">
					Securely share files and folders with friends, family and colleagues for live
					collaboration. No email attachments required!
				</p>
				<div class="middle-link">
					<a href="#">See how Fylo works </a>
					<img src="./images/icon-arrow.svg" alt="" />
				</div>
			</div>
		</div>
	</div>
</div>
<div class="cardContainer">
	<img class="imgQuotes" src="images/bg-quotes.png" alt="" />
	<div class="cardContent">
		<p>
			Fylo has improved our team productivity by an order of magnitude. Since making the switch our
			team has become a well-oiled collaboration machine.
		</p>
		<div class="quote-author">
			<img src="images/profile-1.jpg" alt="" />
			<div class="authors">
				<span class="author-name">Satis Patel</span><br />
				<span class="author-title">Founder & CEO, Huddle</span>
			</div>
		</div>
	</div>
	<div class="cardContent">
		<p>
			Fylo has improved our team productivity by an order of magnitude. Since making the switch our
			team has become a well-oiled collaboration machine.
		</p>
		<div class="quote-author">
			<img src="images/profile-2.jpg" alt="" />
			<div class="authors">
				<span class="author-name">Bruce McKenzie</span><br />
				<span class="author-title">Founder & CEO, Huddle</span>
			</div>
		</div>
	</div>
	<div class="cardContent">
		<p>
			Fylo has improved our team productivity by an order of magnitude. Since making the switch our
			team has become a well-oiled collaboration machine.
		</p>
		<div class="quote-author">
			<img src="images/profile-3.jpg" alt="" />
			<div class="authors">
				<span class="author-name">Iva Boyd</span><br />
				<span class="author-title">Founder & CEO, Huddle</span>
			</div>
		</div>
	</div>
</div>
<div class="footerContainer">
	<div class="cardFloat">
		<h1 class="floatHeader">Get early access today</h1>
		<p class="floatTxt">
			It only takes a minute to sign up and our free starter tier is extremely generous. If you have
			any questions, our support team would be happy to help you.
		</p>
		<div class="botFloat">
			<input class="floatInput" type="text" placeholder="email@example.com" bind:value={email}/>
			<button class="floatBtn" on:click={handleClick}>Get Started For Free</button>
		</div>
		{#if isError}
			<p class="textError">Please enter a valid emaill address</p>
		{/if}
	</div>
	<div class="footerContent">
		<img class="logoFooter" src="images/logo.svg" alt="" />
		<div class="footerContentLeft">
			<div class="footerContact">
				<div class="contentContact">
					<img class="contactIcon" src="images/icon-location.svg" alt="" />
					<p class="contactTxt">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
						incididunt ut labore et dolore magna aliqua
					</p>
				</div>
			</div>
			<div class="footerContact">
				<div class="contentContact">
					<img class="contactIcon" src="images/icon-phone.svg" alt="" />
					<p class="contactTxt">+1-543-123-4567</p>
				</div>
				<div class="contentContact">
					<img class="emailIcon" src="images/icon-email.svg" alt="" />
					<p class="emailTxt">example@huddle.com</p>
				</div>
			</div>
			<div class="footerContactTwo">
				<div class="footerList">
					<ul>
						<li>About Us</li>
						<li>Jobs</li>
						<li>Press</li>
						<li>Blog</li>
					</ul>
				</div>
				<div class="footerList">
					<ul>
						<li>Contact Us</li>
						<li>Terms</li>
						<li>Privacy</li>
					</ul>
				</div>
			</div>
			<div class="footerContact">
				<div class="sosmed">
					<span><i class="fab fa-facebook-f" /></span>
					<span><i class="fab fa-twitter" /></span>
					<span><i class="fab fa-instagram" /></span>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.navbar {
		display: flex;
		justify-content: space-between;
		padding: 50px;
		align-items: center;
	}

	.menus {
		display: flex;
	}

	.menus ul {
		list-style: none;
		margin: 0;
		padding: 0;
	}

	.headerList {
		float: left;
	}

	.headerList a {
		color: var(--white);
		display: block;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
	}

	.headerList a:hover {
		text-decoration: underline;
	}

	.topContainer {
		width: 100%;
		text-align: center;
		/* padding: 0px 100px 150px 100px; */
		background-image: url('images/bg-curvy-desktop.svg');
		background-repeat: no-repeat;
		background-position: bottom;
		background-size: cover;
		background-size: 100%;
	}

	.topContent {
		width: 100%;
		margin-top: 20px;
		padding: 0px 100px 200px;
		text-align: center;
	}

	.topHeader {
		font-size: 38px;
		padding: 0px 200px;
		line-height: 3rem;
	}

	.topSubtitle {
		margin: 30px 0px;
		padding: 0px 360px;
		letter-spacing: 1px;
		line-height: 1.5rem;
	}

	.btn {
		color: var(--white);
		padding: 12px;
		background-color: var(--blue);
		width: 20%;
		border-radius: 25px;
		opacity: 1;
	}

	.btn:hover {
		background-color: var(--cyan);
		cursor: pointer;
		opacity: 0.8;
	}

	.middleContainer {
		background-color: var(--mainBg);
		padding: 0px 50px;
		width: 100%;
	}

	.middleImg {
		padding: 50px;
		width: 100%;
	}

	.middleImgContent {
		display: flex;
		justify-content: space-evenly;
		align-items: center;
		width: 100%;
		padding: 0px 100px;
	}

	.imgContent {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		width: 50%;
		padding: 0px 100px 50px 100px;
	}

	.imgHeader {
		margin: 10px 0px;
		font-size: 24px;
	}

	.middleImgTwo {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0px 50px;
	}

	.twoContent {
		padding: 50px;
		width: 50%;
	}

	.twoHeader {
		width: 50%;
		line-height: 2.5rem;
	}

	.twoTxt {
		padding: 10px 10px 10px 0px;
	}

	.middle-link {
		display: flex;
		align-items: center;
		padding: 5px 0px;
		font-weight: 400;
		font-size: 17px;
		border-bottom: 1px solid hsl(170, 45%, 43%);
		width: 35%;
		gap: 5px;
		cursor: pointer;
	}

	.middle-link a {
		color: var(--cyan);
		text-decoration: none;
	}

	.middle-link:hover {
		border-bottom: 1px solid var(--white);
	}

	.middle-link a:hover {
		color: var(--white);
	}

	.cardContainer {
		position: relative;
		background-color: var(--mainBg);
		padding: 50px 150px 150px 150px;
		width: 100%;
		display: flex;
		justify-content: space-between;
		gap: 20px;
		z-index: -1;
	}

	.cardContent {
		box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
		border-radius: 10px;
		background-color: var(--testiBg);
		padding: 50px 50px 50px 40px;
		width: 450px;
		height: 250px;
	}

	.cardContent p {
		line-height: 1.5rem;
		padding-top: 10px;
	}

	.imgQuotes {
		position: absolute;
		top: 12px;
		left: 140px;
		z-index: -1;
	}

	.quote-author {
		display: flex;
		align-items: center;
		margin-top: 30px;
	}

	.quote-author img {
		height: 30px;
		width: 30px;
		border-radius: 50%;
		margin-right: 10px;
	}

	.authors {
		font-size: 12px;
	}

	.author-name {
		font-weight: 700;
	}

	.author-title {
		font-weight: 400;
	}

	.cardFloat {
		display: flex;
		flex-direction: column;
		align-items: center;
		position: absolute;
		top: 0;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 45%;
		height: 230px;
		border-radius: 10px;
		border: 1px solid var(--introEmail);
		background-color: var(--introEmail);
		box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
		padding: 50px;
		text-align: center;
		/* z-index: 1 */
	}

	.floatHeader {
		margin-bottom: 20px;
	}

	.floatTxt {
		margin-bottom: 20px;
	}

	.botFloat {
		position: relative;
		display: flex;
		width: 100%;
		gap: 10px;
	}

	.floatInput {
		width: 65%;
		border-radius: 25px;
		padding: 10px;
	}

	.floatInput::placeholder {
		color: grey;
	}

	.floatBtn {
		color: var(--white);
		padding: 10px;
		background-color: var(--blue);
		width: 35%;
		border-radius: 25px;
		opacity: 1;
		cursor: pointer;
	}

	.floatBtn:hover {
		background-color: var(--cyan);
		cursor: pointer;
		opacity: 0.8;
	}

	.textError {
		color: var(--lightRed);
		font-size: 10px;
		position: absolute;
		bottom: 8px;
		left: 65px;
	}

	.footerContainer {
		position: relative;
		padding: 50px 50px 100px 50px;
		background-color: var(--footerBg);
		/* z-index: 0; */
	}

	.footerContent {
		padding: 180px 100px;
	}

	.footerContentLeft {
		display: flex;
		width: 100%;
		justify-content: space-between;
		gap: 10px;
		/* align-items: center; */
	}

	.footerContact {
		margin-top: 30px;
		width: 100%;
	}

	.contentContact {
		display: flex;
		width: 100%;
		margin-top: 20px;
	}

	.contactIcon {
		width: 15px;
		height: 20px;
	}

	.emailIcon {
		width: 20px;
		height: 20px;
	}

	.contactTxt {
		color: var(--white);
		margin-left: 20px;
		line-height: 1.5rem;
	}

	.emailTxt {
		color: var(--white);
		margin-left: 15px;
		line-height: 1.5rem;
	}

	.footerContactTwo {
		margin-top: 10px;
		width: 100%;
		display: flex;
		justify-content: space-between;
	}

	.footerList {
		margin-top: 20px;
		color: var(--white);
		font-weight: 700;
		cursor: pointer;
	}

	.footerList li {
		list-style: none;
		margin-top: 20px;
	}

	.footerList li:hover {
		text-decoration: underline;
	}

	.sosmed {
		margin-top: 10px;
		display: flex;
		justify-content: end;
	}

	.sosmed span {
		padding-right: 10px;
	}

	.sosmed span i {
		height: 35px;
		width: 35px;
		color: var(--white);
		border: 2px solid var(--white);
		border-radius: 50%;
		align-items: center;
		text-align: center;
		cursor: pointer;
		padding: 9px 0;
	}

	.sosmed span i:hover {
		color: var(--pink);
		border: 2px solid var(--pink);
	}
</style>
