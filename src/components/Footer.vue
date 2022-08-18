<template>
    <div class="footer-container">
        <div class="content-container primary-color">
            <div class="content">
                <p class="footer-title fw-bold fs-24">SOCIAL</p>
                <p class="social-icon">
                    <fa :icon="['fab', 'instagram']" size="xl"></fa>Instagram
                </p>
                <p class="social-icon">
                    <fa :icon="['fab', 'twitter']" size="xl"></fa>Twitter
                </p>
                <p class="social-icon">
                    <fa :icon="['fab', 'youtube']" size="xl"></fa>Youtube
                </p>
                <p class="social-icon">
                    <fa :icon="['fab', 'facebook']" size="xl"></fa>Facebook
                </p>
            </div>
            <div class="content">
                <p class="footer-title fw-bold fs-24">ESPORTS</p>
                <p>Privacy Policy</p>
                <p>Terms of Service</p>
                <p>Rankings</p>
                <p>Organizers & Player Support</p>
            </div>
            <div class="content">
                <p class="footer-title fw-bold fs-24">HELP</p>
                <p>Contact us</p>
                <p>Partners</p>
                <p>Services</p>
            </div>
        </div>
    </div>
</template>

<style>
.footer-container {
    background: var(--secondary-bg-color);
}

.content-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: flex-start;
    padding: 25px 0px;
    gap: 250px;
}

.content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 0px;
    gap: 20px;
}

.social-icon svg {
    padding-right: 10px;
}
</style>