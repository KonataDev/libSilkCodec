## libSilkCodec
Cross-platform silk codec wrap library dependents on [silk-v3-decoder](https://github.com/kn007/silk-v3-decoder).

## Build
```bash
  # just make it
  $ cmake . && make -j8

  # or
  $ chmod +x build.sh
  $ ./build.sh
```

## Example
```C
  // Decode silk to pcm
  ret = silkDecode(data, dataLen, 24000, codecCallback);
  if(!ret) return 0xDEADC0DE;

  // Encode pcm to silk
  ret = silkEncode(data, dataLen, 24000, codecCallback);
  if(!ret) return 0xDEADC0DE;

  // Decode or Encode callback
  void codecCallback(unsigned char* p, int len) {
    writeData(p, len);
  }

```

## Todo
- [ ] Callback with userdata

## Credits
- [silk-v3-decoder](https://github.com/kn007/silk-v3-decoder)
