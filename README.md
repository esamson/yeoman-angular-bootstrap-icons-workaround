These are the steps.

1. yo angular --minsafe
    1.1. Would you like to include Twitter Bootstrap? (Y/n) Y
    1.2. If so, would you like to use Twitter Bootstrap for Compass (as opposed to vanilla CSS)? (Y/n) Y
    1.3. Would you like to include angular-resource.js? (Y/n) Y
    1.4. Would you like to include angular-cookies.js? (Y/n) Y
    1.5. Would you like to include angular-sanitize.js? (Y/n) Y

2. grunt

    You get this warning:

        Running "compass:dist" (compass) task
        WARNING: 'glyphicons-halflings.png' was not found (or cannot be read) in /tmp/5425451/app/images
        WARNING: 'glyphicons-halflings-white.png' was not found (or cannot be read) in /tmp/5425451/app/images

3. Add `app/images/glyphicons-halflings-white.png` and `app/images/glyphicons-halflings.png`
