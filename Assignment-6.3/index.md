Here is your complete Assignment 6.3 — Overflow & Layout Fixing in HTML and CSS. It includes all four overflow values, a second scrollable container using overflow: auto, and a sample page with an overflow issue that has been fixed.

Create a file named Assignment-6.3.html, paste the following code into it, and open it in your browser.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.3 - Overflow & Layout Fixing</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f0f4f8;
            color: #333;
            line-height: 1.6;
        }

        h1 {
            text-align: center;
            color: #174a7e;
        }

        h2 {
            color: #174a7e;
        }

        .section {
            max-width: 900px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 2px 8px #00000015;
        }

        /* Fixed-size container */
        .overflow-box {
            height: 150px;
            width: 100%;
            border: 2px solid #174a7e;
            padding: 12px;
            margin-bottom: 20px;
            background-color: #eaf3ff;
        }

        /* Example 1: Visible */
        .visible {
            overflow: visible;
        }

        /* Example 2: Hidden */
        .hidden {
            overflow: hidden;
        }

        /* Example 3: Auto */
        .auto {
            overflow: auto;
        }

        /* Example 4: Scroll */
        .scroll {
            overflow: scroll;
        }

        /* Second scrollable container */
        .second-container {
            height: 180px;
            overflow: auto;
            border: 2px solid #25855a;
            padding: 15px;
            background-color: #e9fff1;
        }

        /* Fixed sample page layout */
        .sample-page {
            width: 100%;
            max-width: 100%;
            overflow-wrap: anywhere;
            border: 2px solid #d28b00;
            padding: 15px;
            background-color: #fff8e6;
        }

        .sample-content {
            width: 100%;
            max-width: 100%;
            overflow-wrap: anywhere;
        }

        .long-text {
            overflow-wrap: anywhere;
        }

        .footer {
            text-align: center;
            margin-top: 30px;
            padding: 15px;
            background-color: #174a7e;
            color: white;
        }
    </style>
</head>

<body>

    <h1>Assignment 6.3</h1>
    <h1>Overflow & Layout Fixing</h1>

    <div class="section">
        <h2>1. Overflow: Visible</h2>
        <p>
            The content is allowed to extend outside the container.
            Notice how the extra text appears beyond the box.
        </p>

        <div class="overflow-box visible">
            <strong>Visible Overflow</strong>
            <p>
                HTML is used to create the structure of a webpage.
                CSS is used to style the webpage and control its layout.
                When overflow is set to visible, extra content is displayed
                outside the fixed-height container. This paragraph contains
                additional text to demonstrate how content can extend beyond
                the bottom boundary of the box.
            </p>
        </div>
    </div>

    <div class="section">
        <h2>2. Overflow: Hidden</h2>
        <p>
            Extra content outside the container is clipped and cannot
            be seen.
        </p>

        <div class="overflow-box hidden">
            <strong>Hidden Overflow</strong>
            <p>
                This is an example of hidden overflow. The container has
                a fixed height of 150 pixels. There is more text than can
                fit inside the box, so the remaining content is hidden.
                The user cannot scroll to see the clipped content.
            </p>
        </div>
    </div>

    <div class="section">
        <h2>3. Overflow: Auto</h2>
        <p>
            A scrollbar appears only when the content needs it.
            Scroll inside the box to read the remaining text.
        </p>

        <div class="overflow-box auto">
            <strong>Auto Overflow</strong>
            <p>
                This container has a fixed height of 150 pixels.
                It contains extra content that exceeds the available space.
                The auto property allows the browser to add scrollbars
                when necessary. This is useful for displaying long text
                without making the entire webpage excessively long.
            </p>
            <p>
                More content is included here to make the container
                scrollable. Keep scrolling to view all the text in this
                example.
            </p>
        </div>
    </div>

    <div class="section">
        <h2>4. Overflow: Scroll</h2>
        <p>
            Scrollbars are provided even when they may not be necessary.
        </p>

        <div class="overflow-box scroll">
            <strong>Scroll Overflow</strong>
            <p>
                This container uses overflow: scroll. Its height is fixed
                at 150 pixels, and its content is longer than the available
                space. Scrollbars let the user access the additional text.
                This property is useful when you want scrolling to be
                available in the container.
            </p>
            <p>
                Additional text ensures that the content overflows.
                Scroll down to read the rest of the paragraph.
            </p>
        </div>
    </div>

    <div class="section">
        <h2>5. Second Scrollable Container</h2>
        <p>
            This container also uses overflow: auto to keep its content
            within a fixed-height area.
        </p>

        <div class="second-container">
            <h3>About Web Development</h3>
            <p>
                Web development involves creating and maintaining websites.
                HTML provides the page structure, CSS controls appearance,
                and JavaScript adds interactive features.
            </p>
            <p>
                Responsive design helps websites work on desktops,
                tablets, and mobile phones. CSS overflow properties help
                developers manage content that does not fit inside a box.
            </p>
            <p>
                This is extra content for testing scrolling. The container
                stays at a fixed height, while users can scroll to access
                all the information without expanding the box.
            </p>
        </div>
    </div>

    <div class="section">
        <h2>6. Sample Page: Overflow Issue Fixed</h2>

        <p>
            Problem: A page can overflow horizontally when an element
            is wider than the screen or contains a very long word.
        </p>

        <p>
            Solution: Use box-sizing: border-box, max-width: 100%,
            and overflow-wrap: anywhere to keep content within its layout.
        </p>

        <div class="sample-page">
            <div class="sample-content">
                <h3>My Sample Webpage</h3>
                <p>
                    This sample layout fits inside its parent container.
                    The width is limited to 100%, and padding is included
                    within the element's total width.
                </p>

                <p class="long-text">
                    Long text test:
                    ThisIsAVeryLongWordWithoutSpacesThatCouldOtherwiseCauseHorizontalOverflowOnTheWebpage
                </p>

                <p>
                    The layout has been fixed so that long text can wrap
                    onto new lines instead of extending beyond the
                    container. The page also adjusts to smaller screens.
                </p>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>7. Conclusion</h2>
        <ul>
            <li><strong>visible:</strong> Extra content extends outside the box.</li>
            <li><strong>hidden:</strong> Extra content is clipped.</li>
            <li><strong>auto:</strong> Scrollbars appear when needed.</li>
            <li><strong>scroll:</strong> Scrollbars are provided for scrolling.</li>
            <li><strong>Layout fix:</strong> Content wraps and stays within the available width.</li>
        </ul>
    </div>

    <div class="footer">
        Assignment 6.3 - Overflow & Layout Fixing
    </div>

</body>
</html>



How to run your assignment
1. Open Notepad or Visual Studio Code.
2. Paste the complete code above.
3. Save the file as Assignment-6.3.html (select All Files in Notepad's Save as type).
4. Double-click the saved file to open it in Chrome.
5. Test the visible, hidden, auto, and scroll examples. For the auto and scroll boxes, scroll inside the box to view the remaining text.
Screenshot for submission
Take a screenshot of the webpage showing the overflow examples and the fixed sample layout.
- Windows shortcut: Win + Shift + S
- Capture the browser page and save the image as Assignment-6.3-Screenshot.png.
- If the whole assignment does not fit on the screen, take two or more screenshots while scrolling down the page.
Your submission will include: the HTML file and the screenshot(s) demonstrating each overflow value and the corrected layout.











Do you like this personality?