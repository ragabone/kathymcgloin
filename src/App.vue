<script setup>
import frontCover from "./assets/Front Cover.png";
import authorProfile from "./assets/author_profile.jpg";

const navigation = [
	{ label: "The Book", href: "#book" },
	{ label: "Launch", href: "#launch" },
	{ label: "Author", href: "#author" },
	{ label: "Where to Buy", href: "#buy" },
];

const stockists = [
	{
		name: "Liber Bookshop",
		location: "Sligo, County Sligo",
		website: "https://liber.ie/",
	},
	{ name: "The Wishing Chair", location: "Bundoran, County Donegal" },
	{ name: "The American House", location: "Bundoran, County Donegal" },
	{ name: "A Novel Idea Bookshop", location: "Ballyshannon, County Donegal" },
	{ name: "Four Masters Bookshop", location: "Donegal Town, County Donegal" },
];
</script>

<template>
	<header class="site-header">
		<a class="brand" href="#top" aria-label="Second Chances by the Sea home">
			<span>Second Chances</span>
			<small>by the Sea</small>
		</a>
		<nav aria-label="Main navigation">
			<a v-for="item in navigation" :key="item.href" :href="item.href">{{
				item.label
			}}</a>
		</nav>
	</header>

	<main id="top">
		<section class="hero" aria-labelledby="hero-title">
			<div class="hero-copy">
				<p class="eyebrow">Kathy McGloin’s debut novel</p>
				<h1 id="hero-title">Second Chances<br /><em>by the Sea</em></h1>
				<p class="tagline">
					Sometimes the tide brings you back to where you belong.
				</p>
				<a class="button" href="#book"
					>Discover the story <span aria-hidden="true">↓</span></a
				>
			</div>
			<div class="cover-wrap">
				<img
					class="cover-image"
					:src="frontCover"
					alt="Front cover of Second Chances by the Sea by Kathy McGloin"
				/>
			</div>
		</section>

		<section
			id="book"
			class="section story-section"
			aria-labelledby="book-title"
		>
			<div class="section-label">The story</div>
			<div>
				<h2 id="book-title">A new shore. A fresh start.</h2>
				<p class="lead">
					After a devastating betrayal shatters the life she thought she was
					building in Belfast, Erin escapes to the seaside town of Bundoran on
					Ireland’s west coast, hoping only for a fresh start and a little
					peace.
				</p>
				<p class="muted">
					<strong>Genre:</strong> Romantic fiction, set between Belfast and
					Ireland’s west coast.
				</p>
			</div>
		</section>

		<section id="launch" class="launch-section" aria-labelledby="launch-title">
			<div class="launch-intro">
				<p class="eyebrow">You’re invited</p>
				<h2 id="launch-title">Book launch</h2>
				<p>
					Join Kathy McGloin to celebrate <em>Second Chances by the Sea</em>.
				</p>
			</div>
			<div class="launch-details">
				<p class="date">Wednesday<br /><strong>September 9, 2026</strong></p>
				<p>
					<strong>18:30</strong><br />Marc Geagan Suite<br />Bundoran Community
					Centre<br />Bundoran, County Donegal
				</p>
				<p class="refreshments">Refreshments served</p>
			</div>
		</section>

		<section
			id="author"
			class="section author-section"
			aria-labelledby="author-title"
		>
			<img class="author-photo" :src="authorProfile" alt="Kathy McGloin" />
			<div>
				<div class="section-label">The author</div>
				<h2 id="author-title" class="author-name">Kathy McGloin</h2>
				<p class="lead">
					Kathy McGloin grew up in Belfast during the Troubles of the 1970s,
					’80s and ’90s, spending her childhood summers caravanning in the
					idyllic seaside town of Bundoran, on the west coast of Ireland — a
					place that became a sanctuary for her family and has remained close to
					her heart ever since.
				</p>
				<p class="muted">
					Inspired by those memories of the Donegal coast,
					<em>Second Chances by the Sea</em> is her debut novel — a heartfelt
					story about healing, hope, and finding home in unexpected places.
				</p>
				<p class="muted">
					Kathy now lives in Bundoran with her husband, James, whose constant
					love and encouragement supported her throughout her writing journey.
					Her twin sons, Michael and Oisín, who are currently studying abroad,
					have also been among her biggest supporters. The Atlantic Ocean
					continues to inspire her every single day.
				</p>
			</div>
		</section>

		<section class="setting-section" aria-labelledby="setting-title">
			<div>
				<p class="eyebrow">The setting</p>
				<h2 id="setting-title">At the edge of the Atlantic</h2>
				<p>
					Bundoran, on Ireland’s west coast, and its striking Fairy Bridges form
					an important part of the novel’s coastal atmosphere.
				</p>
			</div>
			<figure class="setting-image">
				<img
					src="https://cdn.shopify.com/s/files/1/0274/3963/files/image-1300x1000_480x480.png"
					alt="The Fairy Bridges on the Bundoran coast"
				/>
				<figcaption>Bundoran &amp; the Fairy Bridges</figcaption>
			</figure>
		</section>

		<section id="buy" class="section buy-section" aria-labelledby="buy-title">
			<div class="section-label">Find your copy</div>
			<div>
				<h2 id="buy-title">Where to buy</h2>
				<p class="lead">Available locally from these independent stockists.</p>
				<div class="stockists">
					<article
						v-for="stockist in stockists"
						:key="stockist.name"
						class="stockist"
					>
						<h3>{{ stockist.name }}</h3>
						<p>{{ stockist.location }}</p>
						<a
							v-if="stockist.website"
							:href="stockist.website"
							target="_blank"
							rel="noreferrer"
							>Visit shop website <span aria-hidden="true">↗</span></a
						>
						<span v-else>In-store stockist</span>
					</article>
				</div>
				<p class="purchase-note">
					Please contact the individual shop to check current stock
					availability.
				</p>
			</div>
		</section>
	</main>

	<footer class="site-footer">
		<p><strong>Second Chances by the Sea</strong> &mdash; Kathy McGloin</p>
		<div class="footer-links" aria-label="Contact and social links">
			<a href="mailto:kmcgloin31@gmail.com">Email Kathy</a>
			<a
				href="https://www.instagram.com/kathy._54321?utm_source=qr&amp;igsi=bmhtMXkzYXY3eTVp"
				target="_blank"
				rel="noreferrer"
				>Instagram <span aria-hidden="true">↗</span></a
			>
			<a
				href="https://www.facebook.com/share/19GE6iTKLP/"
				target="_blank"
				rel="noreferrer"
				>Facebook <span aria-hidden="true">↗</span></a
			>
		</div>
	</footer>
</template>
