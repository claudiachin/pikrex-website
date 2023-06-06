<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Akshar:wght@300;700&display=swap');

    $black: #121212;
    $dark_grey: #404040;
    $white: #FFFFFF;
    $pink: #ED3996;
    $light_pink: #FAC7E1;
    $dark_pink: #D51477;
    $opaque: rgba(0,0,0,0);

    // "Global" styles
    .emphasis {
        color: $pink;
    }

    .button {
        display: flex;
        gap: 8px;
        justify-content: center;
        align-items: center;
        border-radius: 1000px;
        padding: 8px 32px;
        border: 2px solid $pink;
        width: max-content;    

        &:hover {
            border: 2px solid $dark-pink;
        }

        i {
            font-size: 16px;
            color: $white;
        }
    }
    .outline {
        background-color: $opaque;
    }
    .filled {
        background-color: $pink;
        &:hover {
            background-color: $dark-pink;
        }
    }
    .light {
        .filled {
            p {
                color: $white;
            }
        }
    }

    .button-group {
        display: flex;
        gap: 20px;
    }

    .text-group-center {
        display: flex;
        flex-direction: column;
        gap: 12px;
        justify-content: center;
        align-items: center;
        
        h3, p {
            text-align: center;
        }
    }
    .text-group-right {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }
    
    // Section styling
    .section {
        padding: 32px;
    }

    // Header styling
    .header {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        justify-items: center;
        align-items: center;
        background-color: $black;

        img {
            height: 48px;
        }
        .switch {
            justify-self: end;
        }
    }

    .switch {
        label {
            position: relative;
            display: inline-block;
            width: 60px;
            height: 36px;
            background-color: $dark_grey;
            border-radius: 50px;
            cursor: pointer;
        }

        input {
            position: absolute;
            display: none;
        }

        .slider {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50px;
            transition: 0.3s;
        }

        input:checked ~ .slider {
            background-color: $pink;
        }

        .slider::before {
            content: "";
            position: absolute;
            top: 4px;
            left: 5px;
            width: 28px;
            height: 28px;
            border-radius: 50%;
            box-shadow: inset 6px -2px 0px 0px $pink;
            background-color: $dark_grey;
            transition: 0.3s;
        }

        input:checked ~ .slider::before {
            transform: translateX(22px);
            background-color: $dark_grey;
            box-shadow: none;
        }
    }

    // Main body styling
    .light {
        .main-body {
            background: $white;
        }

        h1, h2, h3, h4, h5, h6, p, label, input {
            color: $black;
        }
    }
    
    .dark {
        .main-body {
            background: $black;
        }

        h1, h2, h3, h4, h5, h6, p, label, input {
            color: $white;
        }
    }

    // Hero Styling
    #hero {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        justify-content: center;
        align-items: center;

        .hero-img {
            flex: 0 1 500px;
        }

        img {
            width: 100%;
        }

        .text-group-right {
            flex: 0 1 400px;
        }
    }

    // Details styling
    #details {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 20px;
    }
    .light {
        #details {
            i {
                color: $black;
            }
        }
    }

    .detail {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;

        i {
            font-size: 24px;
            color: $white;
        }
    }

    // Pricing styling
    #pricing {
        display: flex;
        flex-direction: column;
        gap: 40px;
    }
    .light {
        #pricing{
            .pricing-item {
                h2, h5, p {
                    color: $white;
                }

                &:nth-child(2) {
                    background: linear-gradient($pink, $black);
                }
            }
        }
    }
    
    .pricing-list {
        display: grid;
        gap: 24px;
        overflow-x: auto;
        grid-auto-flow: column;
        overscroll-behavior-x: auto;
        scroll-snap-type: x mandatory;
        -webkit-overflow-scrolling: touch;

        &::-webkit-scrollbar {
            height: 44px;
        }
        &::-webkit-scrollbar-thumb {
            background: $pink; 
            border-radius: 1000px;
            border: 20px solid rgba(0, 0, 0, 0);
            background-clip: padding-box;
        }
    }
    .pricing-item {
        padding: 32px 24px;
        border-radius: 8px;
        background: linear-gradient($black, $dark_grey);

        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
        justify-content: space-between;

        min-width: 300px;
        scroll-snap-align: center;

        > div {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 16px;
        }

        &:nth-child(2) {
            background: linear-gradient($pink, $light_pink);
        }
    }
    .price {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .pricing-details {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 8px;
    }
    .p-detail {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 12px;

        i {
            font-size: 16px;
            color: $white;
        }
    }

    // Clients styling
    #clients {
        display: flex;
        flex-direction: column;
        gap: 40px;
    }

    .clients-list {
        display: flex;
        justify-content: center;
        gap: 80px;
        flex-wrap: wrap;
    }

    .client {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 12px;

        h4 {
            color: $pink;
        }
    }

    // Feature styling
    .feature {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        justify-content: center;
        align-items: center;

        .feature-img {
            flex: 0 1 440px;
        }

        img {
            width: 100%;
        }

        .text-group-right {
            flex: 0 1 440px;
        }
    }

    // Contact Us styling
    #contact-us {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 40px;

        form {
            width: 100%;
            max-width: 700px;

            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }

        .form-row {
            width: 100%;
            display: flex;
            gap: 20px;
        }
        .row-1 {
            .form-item {
                width: 50%;
            }
        }
        .row-2 {
            .form-item {
                width: 100%;
            }
        }

        .form-item {
            label {
                color: $light_pink;
            }
            input {
                width: 100%;
                background-color: transparent;
                border: none;
                border-bottom: 2px solid $pink;
                outline: none;
                font-size: 16px;
                margin-top: 8px;
            }
        }

        #submit {
            margin-top: 20px;
            font-size: 16px;
            color: $white;
        }
    }

    // Footer styling
    .footer {
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;
        background-color: $black;

        > div {
            display: flex;
            gap: 16px;
        }

        img {
            height: 36px;
        }
    }
    .light {
        .footer {
            p {
                color: $white;
            }
        }
    }

</style>

<script>
    let light = false;
</script>

<div class={light ? 'light' : 'dark'}>

<div class="section header">
    <div></div>
    <img src="/logo-icon.png" alt="logo"/>
    <div class="switch">
        <label>
            <input type="checkbox" bind:checked={light}>
            <span class="slider"></span>
        </label>
    </div>
</div>

<div class="main-body">

    <div id="hero" class="section">
        <div class="hero-img">
            <img src={light ? "/people-and-technology-light.svg" : "/people-and-technology-dark.svg"} alt="logo"/>
        </div>
        <div class="text-group-right">
            <h1>Great translation at <span class="emphasis">an unbeatable price</span>.</h1>
            <p>Pikrex offers great quality translation services in Japanese, French, Spanish, and Korean, starting at $0.</p>
            <div class="button-group">
                <a href="#pricing"><button class="button filled"><p>Our Pricing</p></button></a>
                <a href="#contact-us"><button class="button outline"><p>Contact Us</p></button></a>
            </div>
        </div>
    </div>

    <div id="details" class="section">
        <div class="detail"><i class="fa-solid fa-check"></i><h6>Translates Japanese, French, Spanish, and Korean seamlessly</h6></div>
        <div class="detail"><i class="fa-solid fa-check"></i><h6>Fast and easy set up -- add it to your project instantaneously</h6></div>
        <div class="detail"><i class="fa-solid fa-check"></i><h6>Expanded customisation for Translation API</h6></div>
    </div>

    <div id="pricing" class="section">
        <div class="text-group-center">
            <h3>Compare our plans</h3>
            <p>Pikrex offers multiple plans for you to choose from to power your projects.</p>
        </div>
        <div class="pricing-list">
            <div class="pricing-item">
                <div>
                    <h5>Free</h5>
                    <div class="price">
                        <h2>$0</h2>
                        <p>per million characters</p>
                    </div>
                    <div class="pricing-details">
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                    </div>
                </div>
                <a href="#contact-us"><button class="button filled"><p>Contact Us</p></button></a>
            </div>
            <div class="pricing-item">
                <div>
                    <h5>Pro</h5>
                    <div class="price">
                        <h2>$10</h2>
                        <p>per million characters</p>
                    </div>
                    <div class="pricing-details">
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod</p></div>
                    </div>
                </div>
                <a href="#contact-us"><button class="button filled"><p>Contact Us</p></button></a>
            </div>
            <div class="pricing-item">
                <div>
                    <h5>Business</h5>
                    <div class="price">
                        <h2>TBD</h2>
                        <p>per million characters</p>
                    </div>
                    <div class="pricing-details">
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                        <div class="p-detail"><i class="fa-solid fa-check"></i><p>Lorem ipsum dolor sit amet, consectetur</p></div>
                    </div>
                </div>
                <a href="#contact-us"><button class="button filled"><p>Contact Us</p></button></a>
            </div>
        </div>
    </div>

    <div id="clients" class="section">
        <div class="text-group-center">
            <h3>Our satisfied clients</h3>
            <p>Pikrex has empowered our client to reach out to wider audiences with the power of quality translations.</p>
        </div>
        <div class="clients-list">
            <div class="client">
                <img src="/dreamsavior-logo.png" alt="dreamsavior.net" />
                <h6>DreamSavior.net</h6>
                <h4>5,000+ users</h4>
            </div>
            <div class="client">
                <img src="/adventcirno-logo.png" alt="adventcirno" />
                <h6>Advent Cirno</h6>
                <h4>20,000+ users</h4>
            </div>
            <div class="client">
                <img src="/ichigo-logo.png" alt="ichigo manga translator" />
                <h6>Ichigo Manga Translator</h6>
                <h4>10,000+ users</h4>
            </div>
        </div>
    </div>

    <div id="feature-1" class="section feature">
        <div class="text-group-right">
            <h3>Get started with Pikrex in <span class="emphasis">less than 5 minutes</span>.</h3>
            <p>Setting up Pikrex for your project takes less than 5 minutes. All need to start a new project or integrate it into your existing project is 3 simple steps.</p>
            <a href="https://github.com/leminhyen2/Sugoi-Japanese-Translator" target="_blank"><button class="button outline"><p>GitHub</p><i class="fa-brands fa-github button-icon"></i></button></a>
        </div>
        <div class="feature-img">
            <img src={light ? "/instructions-light.svg" : "/instructions-dark.svg"} alt="logo"/>
        </div>
    </div>

    <div id="feature-2" class="section feature">
        <div class="feature-img">
            <img src={light ? "/translation-light.svg" : "/translation-dark.svg"} alt="logo"/>
        </div>
        <div class="text-group-right">
            <h3><span class="emphasis">Translate reviews</span> on your website.</h3>
            <p>The Pikrex API gives you the power to customise the translations you need on your website to give you the most efficient and effective workflows.</p>
        </div>
    </div>

    <div id="contact-us" class="section">
        <div class="text-group-center">
            <h3>Interested to find out more?</h3>
            <p>Talk to our sales associates to figure out what is the best plan for you.</p>
        </div>
        <form>
            <div class="form-row row-1">
                <div class="form-item">
                    <label for="name">Name *</label><br>
                    <input type="text" id="name" name="name" required placeholder="e.g. John Doe">
                </div>
                <div class="form-item">
                    <label for="email">Email *</label><br>
                    <input type="email" id="email" name="email" required placeholder="e.g. abc@gmail.com">
                </div>
            </div>
            <div class="form-row row-2">
                <div class="form-item">
                    <label for="purpose">Purpose</label><br>
                    <input type="text" id="purpose" name="purpose" placeholder="Tell us more about how you would use Pikrex, etc.">
                </div>
            </div>
            <input class="button filled" type="submit" id="submit" value="Submit">
        </form>
    </div>

</div>

<div class="section footer">
    <div>
        <img src="/logo-icon.png" alt="logo-icon"/>
        <img src="/logo-asset.png" alt="logo-icon"/>
    </div>
    <p>Copyright 2023. Pikrex Inc.</p>
</div>

</div>