# spotify_strobe
creating an SCCS strobe sequence aligning with the frequencies (minus a perfect third for greater intermodulation distortion) and amplitudes of each time slice within any Spotify song per a free public Spotify API

This script requires manual entry of output within the "segments" matrix from a Spotify API spectral data analyser found at: https://developer.spotify.com/documentation/web-api/reference/get-audio-analysis#_=_

After manually editing that data to account for such changes as { to struct(, } to ), ^p to , and " to ', pitch and loudness are pulled from the matrix.

Values for pitch are then transmuted into the corresponding frequencies for the C-1 to B-1 range ("subsubcontra"), transposed down one major third from Ab-2 to G-1 for greater intermodulation distortion between auditory and visual information, and the aligned with the "pitch" value in our spectral data matrix to associate the frequency of the light with each change in dominant note per time slice.

Loudness is transformed into amplitude by correcting for the API's -60 dB suppression, and then made relative to the 0-255 brightness spectrum of the light so that the loudest moments of each song are met with the maximum intensity of the strobe light.

Frequency and amplitude per time sample are then fed into a periodic strobosopic stimulation sequence for the SCCS research strobe.

This repository contains one example of this script in action to Holst's "Jupiter, the Bringer of Jollity" from The Planets, Op. 32, jupiter.m.

as well as an entire "concert experience", experience.m 
