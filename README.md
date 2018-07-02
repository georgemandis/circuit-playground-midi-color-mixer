# Circuit Playground MIDI Controller — Color Mixer

This is designed to work with the [Circuit Playground MIDI Controller Multi-Tool](https://github.com/georgemandis/circuit-playground-midi-multi-tool) — a project designed for my [WebMIDI workshops](http://midi.mand.is/) that turns your Adafruit Circuit Playground into a fun, multi-faceted MIDI controller. There are 10 different MIDI modes once the sketch is uploaded. This demo makes use of **Mode #10** (RGB color mixing).

This WebMIDI demo makes use of Mode #10 to manipulate the onboard RGB NeoPixel LEDs and mix colors using a web interface. We do this by sending "noteOn" messages to channels 1-3 for red, green and blue values respectively.  In this mode the device is set to listen for status bytes from 144, 145 and 146 — "noteOn" messages for MIDI channels 1-3 — and the value for each color is the sum of the two data bytes.

The color of all 10 rings should match the swatch on the page as you manipulate the colors.

There is a CodePen setup to test this code here:
https://codepen.io/georgemandis/pen/xjzXgd