<script lang="ts">
	import "./app.css";
	import { Button, buttonVariants } from "$lib/components/ui/button/index.js";
	import * as Dialog from "$lib/components/ui/dialog/index.js";
	import { Input } from "$lib/components/ui/input/index.js";
	import { Label } from "$lib/components/ui/label/index.js";
	import { Textarea } from "$lib/components/ui/textarea/index.js";
</script>

<svelte:head>
	<title>Pasta - Faster, Smarter Government Construction</title>
</svelte:head>

<main
	class="flex flex-col items-center justify-center min-h-screen bg-gray-100"
>
	<div class="bg-white shadow-lg rounded-xl p-8 max-w-xl w-full text-center">
		<h1
			class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl"
		>
			PASTA
		</h1>
		<h2
			class="scroll-m-20 border-b pb-2 text-3xl font-semibold tracking-tight transition-colors first:mt-0"
		>
			Faster, Smarter Government Construction
		</h2>
		<p class="leading-7 [&:not(:first-child)]:mt-6">
			Project management built for efficiency, clarity, and government
			compliance.
		</p>
		<p class="leading-7 [&:not(:first-child)]:mt-6">
			Streamline workflows, track budgets, and manage contractor
			collaboration with ease.
		</p>

		<!-- <Button class="mt-4" on:click=""{() => alert('Sign-up feature coming soon!')}>Get Started</Button> -->
		<!-- <Button onclick={() => toast("Sign-up feature coming soon!")}>Get Started</Button> -->
		<Dialog.Root>
			<Dialog.Trigger class={buttonVariants({ variant: "default" })}
				>Get Started</Dialog.Trigger
			>
			<Dialog.Content class="sm:max-w-[425px]">
				<Dialog.Header>
					<Dialog.Title>Sign Up for Early Access</Dialog.Title>
					<Dialog.Description>
						
					</Dialog.Description>
				</Dialog.Header>
				<div class="grid gap-4 py-4">
					<div class="grid grid-cols-4 items-center gap-4">
						<Label for="name" class="text-right">Name</Label>
						<Input
							id="name"
							value="Pedro Duarte"
							class="col-span-3"
						/>
					</div>
					<div class="grid grid-cols-4 items-center gap-4">
						<Label for="username" class="text-right">Challenges</Label>
						<!-- <Input
							id="username"
							value="@peduarte"
							class="col-span-3"
						/> -->
						<div class="grid w-full gap-2">
							<Textarea id="challenges" placeholder="What challenges do you face in government property project management?" />
							<!-- <Button>Send message</Button> -->
						</div>
						<!-- <Textarea id="challenges" placeholder="What challenges do you face in government property project management?" /> -->
					</div>
				</div>
				<Dialog.Footer>
					<Button type="submit">Sign Up</Button>
				</Dialog.Footer>
			</Dialog.Content>
		</Dialog.Root>

		<div class="grid grid-cols-2 gap-4 mt-6">
			<div class="bg-gray-200 p-4 rounded-lg text-gray-900">
				Project Tracking
			</div>
			<div class="bg-gray-200 p-4 rounded-lg text-gray-900">
				Financial Oversight
			</div>
			<div class="bg-gray-200 p-4 rounded-lg text-gray-900">
				Contractor Collaboration
			</div>
			<div class="bg-gray-200 p-4 rounded-lg text-gray-900">
				Automated Workflows
			</div>
			<div class="bg-gray-200 p-4 rounded-lg text-gray-900">
				Government Compliance
			</div>
			<div class="bg-gray-200 p-4 rounded-lg text-gray-900">
				Data Security
			</div>
		</div>

		
		<!-- <Dialog>
			<h3 class="text-lg font-semibold text-gray-800 mt-6">Sign Up for Early Access</h3>
			<form class="flex flex-col gap-4 mt-4">
				<Input type="text" placeholder="Full Name" required="" />
				<Input type="email" placeholder="Work Email" required="" />
				<Textarea placeholder="What challenges do you face in government project management?" rows="4" required="" />
				<Button type="submit">Sign Up</Button>
			</form>
		</Dialog> -->
	</div>
</main>
