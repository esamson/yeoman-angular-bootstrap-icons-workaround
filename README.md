These are the steps.

1. yo angular --minsafe

    1. Would you like to include Twitter Bootstrap? (Y/n) Y
    2. If so, would you like to use Twitter Bootstrap for Compass (as opposed to vanilla CSS)? (Y/n) Y
    3. Would you like to include angular-resource.js? (Y/n) Y
    4. Would you like to include angular-cookies.js? (Y/n) Y
    5. Would you like to include angular-sanitize.js? (Y/n) Y

2. grunt

    You get this warning:

        Running "compass:dist" (compass) task
        WARNING: 'glyphicons-halflings.png' was not found (or cannot be read) in /tmp/5425451/app/images
        WARNING: 'glyphicons-halflings-white.png' was not found (or cannot be read) in /tmp/5425451/app/images

3. Add `app/images/glyphicons-halflings-white.png` and `app/images/glyphicons-halflings.png`

4. grunt

    Generated CSS, `dist/styles/7079bc05.main.css` includes `app` in the background image URL.

        background-image:url(../../app/images/glyphicons-halflings.png?1366453617)
        background-image:url(../../app/images/glyphicons-halflings-white.png?1366453617)

    Same is observed when running on `grunt server`.

5. Try workaround from https://github.com/yeoman/yeoman/issues/419#issuecomment-14488128

    Generated CSS, `dist/styles/26a753e4.main.css` now contains the expected URLs.

        background-image:url(../images/53f46de4.glyphicons-halflings.png?1366453617)
        background-image:url(../images/5d462625.glyphicons-halflings-white.png?1366453617)
