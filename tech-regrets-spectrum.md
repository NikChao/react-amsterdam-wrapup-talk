# Tech regrets at spectrum
### Max Stoiber

- Spectrum is an open source chat client

### React native web
- Take react-native code and render it in browsers
- started with web, but knew that mobile had to happen
- had to rebuild stuff from scratch
- would've made sense to go mobile first
- mobile experience on desktop is fine, but other way around doesn't make sense

### Not using Next.js
- Next.js is the greatest thing of all time
- needed SSR
- struggled to get SSR to be reliable
- Used for Max's new projects, very solid
- use off the shelf solutions to problems you do not understand deeply

### Using rethink db
- Everything in spectrum is real time
- change feeds, listen to changes in any query
- didn't have good community/support/usage so lots of time spent to understand it
- change feeds don't scale
- should've written pub/sub layer
- carefully choose core tech that is hard to change later
- prioritise community size/active maintenance

### Using DraftJS and WYSIWYG editing
- should've just used their MD editor (fits their audience of developers)
- conservative choices
- don't go for shiniest features
- be open with roadmaps