        /* Pop-up Ad Banner Styles */
        #ad-popup-banner {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: white; /* Light mode default */
            color: var(--light-text);
            padding: 1.5rem;
            border-radius: 1rem;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            z-index: 1500; /* Above regular content, below modals */
            max-width: 90%;
            width: 450px;
            text-align: center;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.5s ease-in-out, visibility 0.5s ease-in-out;
        }
        #ad-popup-banner.show {
            opacity: 1;
            visibility: visible;
        }
        html.dark #ad-popup-banner {
            background-color: var(--dark-bg-card); /* Dark mode */
            color: var(--dark-text);
        }
        #ad-popup-banner .close-btn {
            position: absolute;
            top: 0.75rem;
            right: 0.75rem;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--fg); /* Inherit text color */
            transition: color 0.2s ease, opacity 0.3s ease, visibility 0.3s ease; /* Added transition for smooth appearance */
            opacity: 0; /* Initially hidden */
            visibility: hidden; /* Initially hidden */
        }
        #ad-popup-banner .close-btn.show {
            opacity: 1;
            visibility: visible;
        }
        #ad-popup-banner .close-btn:hover {
            color: var(--main-blue);
        }
        html.dark #ad-popup-banner .close-btn {
            color: var(--dark-text);
        }
        html.dark #ad-popup-banner .close-btn:hover {
            color: var(--light-blue);
        }
        #ad-popup-banner h3 {
            font-size: 1.75rem; /* text-2xl */
            font-weight: 600; /* font-semibold */
            margin-bottom: 1rem;
            color: var(--main-blue); /* Blue title */
        }
        html.dark #ad-popup-banner h3 {
            color: var(--light-blue);
        }
        #ad-popup-banner p {
            font-size: 1rem; /* text-base */
            margin-bottom: 1.25rem;
            color: var(--light-text);
        }
        html.dark #ad-popup-banner p {
            color: var(--dark-text);
        }
        .ad-content-placeholder {
            background-color: #f0f4f8; /* Light gray for light mode */
            padding: 1rem;
            border-radius: 0.5rem;
            min-height: 100px; /* Minimum height for ad content */
            display: flex;
            align-items: center;
            justify-content: center;
            font-style: italic;
            color: #6b7280; /* text-gray-500 */
            transition: background-color 0.3s ease;
        }
        html.dark .ad-content-placeholder {
            background-color: #4a5568; /* Darker gray for dark mode */
            color: #a0aec0; /* Lighter text for dark mode */
        }

         <!-- Pop-up Ad Banner -->
    <div id="ad-popup-banner">
        <button class="close-btn" aria-label="Close Ad">&times;</button>
        <h3 data-translate-key="adsTitle">Reklama</h3>
        <p data-translate-key="adsPopupMessage">Sayohatlaringiz uchun eng yaxshi takliflar!</p>
        <div class="ad-content-placeholder">
            <!-- Bu yerga Google Ads kodini joylashtiring -->
            <!-- Example: <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script> -->
            <!-- <ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-YOUR_PUBLISHER_ID" data-ad-slot="YOUR_AD_SLOT_ID" data-ad-format="auto" data-full-width-responsive="true"></ins> -->
            <!-- <script>(adsbygoogle = window.adsbygoogle || []).push({});</script> -->
            <!-- Reklama kontenti bu yerda ko'rsatiladi -->
        </div>
    </div>


                // Pop-up Ad Banner elements
            const adPopupBanner = document.getElementById('ad-popup-banner');
            const closeAdBtn = adPopupBanner.querySelector('.close-btn');
            let adTimer; // To store the interval for showing ads
            let adDisplayTimeout; // To store the timeout for hiding ads
            let closeButtonTimeout; // To store the timeout for showing the close button

            // Function to show the ad banner
            function showAdBanner() {
                adPopupBanner.classList.add('show');
                closeAdBtn.classList.remove('show'); // Ensure close button is hidden initially

                // Show close button after 10 seconds
                closeButtonTimeout = setTimeout(() => {
                    closeAdBtn.classList.add('show');
                }, 10000); // Close button appears after 10 seconds

                // Hide ad after 15 seconds (total ad display time)
                adDisplayTimeout = setTimeout(() => {
                    adPopupBanner.classList.remove('show');
                    closeAdBtn.classList.remove('show'); // Hide close button when ad hides
                    // Start timer for the next ad after this one hides
                    adTimer = setTimeout(showAdBanner, (3.5 * 60 * 1000)); // Next ad after 3.5 minutes (210 seconds)
                }, 15000); // Ad displays for 15 seconds
            }

            // Function to hide the ad banner
            function hideAdBanner() {
                adPopupBanner.classList.remove('show');
                closeAdBtn.classList.remove('show'); // Hide close button
                clearTimeout(adDisplayTimeout); // Clear any pending hide timeouts
                clearTimeout(closeButtonTimeout); // Clear any pending close button show timeouts
                clearTimeout(adTimer); // Clear any pending ad show timeouts
                // If manually closed, restart the timer for the next ad after the typical hide duration
                adTimer = setTimeout(showAdBanner, (3.5 * 60 * 1000)); // Next ad after 3.5 minutes (210 seconds)
            }

            // Start showing ads: first ad after 30 seconds
            setTimeout(() => {
                showAdBanner();
            }, 30000); // First ad appears after 30 seconds

            // Close button for ad banner
            closeAdBtn.addEventListener('click', () => {
                hideAdBanner();
            });