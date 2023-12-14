<script>
    // transition
    function fade(node, { delay = 100, duration = 300 }) {
        return {
            delay,
            duration,
            css: t => `opacity: ${t}`
        };
    }

    // tab section
    let selectedTab = 'experience'; // default tab

    // Function to switch tabs
    function switchTab(tab) {
        selectedTab = tab;
    }
</script>

<!-- tab selection buttons -->
<div class="flex justify-evenly">
    <button class="p-8 mx-2 text-2xl" on:click={() => switchTab('experience')}>
        Experience
    </button>
    <div class="border-r-2"></div>
    <button class="p-8 mx-2 text-2xl" on:click={() => switchTab('projects')}>
        Projects
    </button>
</div>
<div class="border-b-4"></div>


<!-- tab content -->
{#if selectedTab === 'experience'}
    <div class="container mx-auto px-40 py-20">
        <div class="flex flex-col items-center" transition:fade>
            <h1 class="text-2xl font-medium">Experience</h1>
            <div class="m-8">
                <h2 class="text-xl font-light">Software Engineering Internship</h2>
                <h2 class="text-xl font-light">NI (National Instruments)</h2>
                <h3 class="text-lg font-light">May 2023 - August 2023</h3>
                <h4 class="text-lg font-medium py-2">Overview</h4>
                <p>My Internship was what got me started in getting industry skills relating to software Engineering. I worked with a
                    team of professional software engineers to develop a desktop application for one of the company's testing software.
                    I was able to learn more about desktop development using C# and WPF, as well as gaining experience in working with
                    a VCS and participating in code reviews as the project was constantly evolving.
                </p>
                <h4 class="text-lg font-medium py-2">Impact</h4>
                <p>My Internship was what got me started in getting industry skills relating to software Engineering. I worked with a
                    team of professional software engineers to develop a desktop application for one of the company's testing software.
                    I was able to learn more about desktop development using C# and WPF, as well as gaining experience in working with
                    a VCS and participating in code reviews as the project was constantly evolving.
                </p>
                <h4 class="text-lg font-medium py-2">Skills learned</h4>
                <p>My Internship was what got me started in getting industry skills relating to software Engineering. I worked with a
                    team of professional software engineers to develop a desktop application for one of the company's testing software.
                    I was able to learn more about desktop development using C# and WPF, as well as gaining experience in working with
                    a VCS and participating in code reviews as the project was constantly evolving.
                </p>
            </div>
        </div>
    </div>
{:else if selectedTab === 'projects'}
    <div class="container mx-auto px-40 py-20">
        <div class="flex flex-col items-center" transition:fade>
            <h1 class="text-2xl font-medium">Projects</h1>
            <div class="m-8">
                <h2 class="text-xl font-light">ATrails</h2>
                <h2 class="text-xl font-light">Skills: Mobile Development, Cloud Baas</h2>
                <h3 class="text-lg font-light">November 2023 - December 2023</h3>
                <h4 class="text-lg font-medium py-2">Overview</h4>
                <p>

                </p>
                <h4 class="text-lg font-medium py-2">Impact</h4>
                <p>

                </p>
                <h4 class="text-lg font-medium py-2">Skills learned</h4>
                <p>

                </p>
            </div>
            <div class="m-8">
                <h2 class="text-xl font-light">Goat Places</h2>
                <h2 class="text-xl font-light">Skills: Full Stack Web Development, Cloud PaaS, Cloud DB</h2>
                <h3 class="text-lg font-light">November 2023 - December 2023</h3>
                <h4 class="text-lg font-medium py-2">Overview</h4>
                <p>

                </p>
                <h4 class="text-lg font-medium py-2">Impact</h4>
                <p>

                </p>
                <h4 class="text-lg font-medium py-2">Skills learned</h4>
                <p>

                </p>
            </div>
        </div>
    </div>
{/if}
