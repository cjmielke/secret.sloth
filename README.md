# secret.sloth

Minimal code example for that CTF task that drove you insane

Step 1: use Google lens or tineye to find the original unmodified image
Step 2: Use this code

```
sloth = np.asarray(sloth)[:,:,:3].astype(int)
slothfft=np.fft.fft2(sloth)

orig=Im.open('iHCQX6p.png')         # original sloth image found on reddit
orig = np.asarray(orig).astype(int)

origfft=np.fft.fft2(orig)
fig, ax = plt.subplots(figsize=(18, 30))
out = abs(np.fft.fft2(slothfft-origfft))
out = abs(slothfft-origfft)
print(out.min(), out.max())
#ax.imshow(out/out.max())
out=(out+out.min())
out/=out.max()
ax.imshow(10*out)
#abs(fft).min()
```

