Mithril Live Editing with Electron
==================================

`Electron + Mithril = Live Editing`

Getting Started
---------------

You must have electron installed and on your path.

1. `npm install`
2. `electron . -d` The `-d` is to open dev tools.
3. Edit the `src/components/example.js` view function.
4. Your app will re-render live.  And it will not lose form state.

Caveats
-------

This is a hack.  It works quite well for a specific use case.  But it is still a hack.

- `module.exports` must be a container of functions, not a function itself.
- Instances, like controllers and models, won't be recreated.  This is sort of a good thing?

Thoughts
--------

The idea behind the `patch.js` is not exactly dependent on electron.  And it is
not tied to mithril.  That is just my use case, and so I don't claim it will work in
other situations.

You could use this with React, or canvas or whatever else.
And if you wanted to use this outside of electron, you'd need a server.  But then
you are probably better off checking out an _actual_ solution like Amok.