<script>
    import {
        Button,
        CloseButton,
        Label,
        Input,
        Textarea,
        P,
        A,
    } from "flowbite-svelte";
    import Layout from "./Layout.svelte";
    // import { sineIn } from "svelte/easing";

    // let hidden3 = true;
    // let transitionParams = {
    //     x: -320,
    //     duration: 200,
    //     easing: sineIn,
    // };
</script>

<Layout>
    <div slot="content">
        <form action="#" class="mb-6">
            <div class="mb-6">
                <Label for="email" class="block mb-2">Your email</Label>
                <Input
                    id="email"
                    name="email"
                    required
                    placeholder="name@company.com"
                />
            </div>
            <div class="mb-6">
                <Label for="subject" class="block mb-2">Subject</Label>
                <Input
                    id="subject"
                    name="subject"
                    required
                    placeholder="Let us know how we can help you"
                />
            </div>
            <div class="mb-6">
                <Label for="message" class="mb-2">Your message</Label>
                <Textarea
                    id="message"
                    placeholder="Your message..."
                    rows="4"
                    name="message"
                />
            </div>
            <Button type="submit" class="w-full">Send message</Button>
        </form>
       
    </div>
</Layout>
<!-- <div class="flex items-center">
        <h5
            id="drawer-label"
            class="inline-flex items-center mb-6 text-base font-semibold text-gray-500 uppercase dark:text-gray-400"
        >
            <svg
                class="w-5 h-5 mr-2"
                aria-hidden="true"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
                ><path
                    fill-rule="evenodd"
                    d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z"
                    clip-rule="evenodd"
                /></svg
            >Contact us
        </h5>
        <CloseButton
            on:click={() => (hidden3 = true)}
            class="mb-4 dark:text-white"
        />
    </div> -->
