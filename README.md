# Свеча горела (A Candle Burnt)

Track 9 on «Папа-море» (_Papa-more_, “Father Sea”), by Полуживые (_Poluzhivye_): Vladimir Zakharov Sr.’s song on Boris Pasternak’s «Зимняя ночь», restored with Suno.

On the site: https://vovazakharov.com/music/candle-burnt

## Files

- `candle-burnt_mix.mp3` — the mix, unmastered, as a 320 kbps mp3; the lossless WAV the master was made from is [`father-sea-09-candle-burnt.wav`](https://github.com/vzakharov/vovazakharov.com/releases/download/music-sources/father-sea-09-candle-burnt.wav).
- `candle-burnt.flac` — the master, 24-bit.
- `candle-burnt.master.mp3` — its 320 kbps mp3 copy.
- `mastering/` — the script that made the master: `master.py`, the `spectrum.py` it imports, and their `requirements.txt`.

## How it was mastered

```sh
pip install -r mastering/requirements.txt
curl -LO https://github.com/vzakharov/vovazakharov.com/releases/download/music-sources/father-sea-09-candle-burnt.wav
python mastering/master.py father-sea-09-candle-burnt.wav ref.flac candle-burnt.flac
```

with `ffmpeg` on `PATH` and the reference below saved as `ref.flac`. Half
strength (`master.py`'s default): Matchering matches the mix to the reference,
half of the EQ difference goes onto the mix, and a limiter keeps the decoded
file under -1 dBTP. `master.py`'s docstring has the whole chain.

## The reference

«Прощание» (_Proshchaniye_, “Farewell”), Полуживые, from «Папа-море», at [vovas-music/wangwei@503bb3d](https://github.com/vovas-music/wangwei/blob/503bb3d6141440a3afeb5d07a073a279942383c1/Poluzhivye%20-%20Proshchaniye.flac) — raw download:
https://raw.githubusercontent.com/vovas-music/wangwei/503bb3d6141440a3afeb5d07a073a279942383c1/Poluzhivye%20-%20Proshchaniye.flac

It was picked blind: three catalogue masters each mastered the mix, and the
operator ranked them unlabelled, loudness-matched, before learning which was
which. It is linked rather than copied here, since it already lives in this
organization.
