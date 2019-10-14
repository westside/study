### Features of music
* Zero Crossing Rate : 양음을 왔다갔다하는 rate (메탈 바위소리들이 높음)
   * librosa.zero_crossings 
* Spectral Centroid : 소리의 무게중심 (weighted mean)
   * librosa.feature.spectral_centroid
* Spectral Rolloff: 전체 에너지의 예)85% 에 해당하는 frequency
   * librosa.feature.spectral_rolloff
* MFCC
   * librosa.feature.mfcc
* Chroma Frequencies: 음악의 12음계로 투사되는 피쳐
   * librosa.feature.chroma_stft

![image](https://user-images.githubusercontent.com/1837913/56132420-e0b99c00-5fc4-11e9-9ab0-d96ff3298b19.png)

#### REF
* https://towardsdatascience.com/extract-features-of-music-75a3f9bc265d
* https://towardsdatascience.com/music-genre-classification-with-python-c714d032f0d8


### MFCC란?
* 우선 audio processing에선 멜 필터뱅크까지만 사용해도 괜찮을듯 하다. 
* https://m.blog.naver.com/mylogic/220988857132
* http://practicalcryptography.com/miscellaneous/machine-learning/guide-mel-frequency-cepstral-coefficients-mfccs/
* https://zinniastop.blogspot.com/2017/12/mfcc.html

1. pre-emphasis filtering: s1 = pre-emphasis filter(s)
2. Framing and windowing: s12 = framing(s1), s2 = windowing(s21)
3. Fourier transform and Power spectrum: s3 = fft(s2), s4 = p_spec(s3)
4. Computation of the filterbank: s5 = cal_filterbank(s4)
![image](https://user-images.githubusercontent.com/1837913/56132602-5f163e00-5fc5-11e9-9c1b-390b1013c113.png)
![image](https://user-images.githubusercontent.com/1837913/56132670-8cfb8280-5fc5-11e9-865e-77939b102081.png)
5. Discrete Cosine Transform: s6 = dct(s5)
6. mean normalization:
     Filterbank = mean_norm(s5)
     MFCC = mean_norm(s6)


### MFCC 구현 in c#
* https://github.com/perivar/FindSimilar/blob/master/CoMIRVA/Audio/MFCC.cs
* https://stackoverflow.com/questions/4675457/how-to-generate-the-audio-spectrum-using-fft-in-c
* 참고 : 

```
 public float[] CalculateMelFrequencyCeptrumCoeffiicient(double[] fftMag)
{
    // create 20 log energy values using triangular overlapping windows
    float melWindowSize = 2000.0f / 20.0f;

    for (int i = 0; i < 20; i++)
    {
        // our frequency is 0-4000, so the the mel scale this is about 2000
        float melWindowStart = i * melWindowSize;
        float melWindowEnd = (i + 1) * melWindowSize;
        float linearWindowStart = 700.0f * ((float)Math.Pow(10, melWindowStart / 2595.0f) * -1.0f);
        float linearWindowEnd = 700.0f * ((float)Math.Pow(10, melWindowEnd / 2595.0f) * -1.0f);
        float fftWindowHz = 4000.0f / 64.0f;
        int fftArrayStart = (int)(linearWindowStart / fftWindowHz);
        int fftArrayEnd = (int)(linearWindowEnd / fftWindowHz);

        // now sum fft magnitudes using triangular window

        float N = fftArrayEnd - fftArrayStart;
        for (float f = 0.0f; f < N; f++)
        {
            melLogE = 0.0f;
            melLogE += (float)fftMag[fftArrayStart + (int)f] * (2.0f / (N - 1.0f) * ((N - 1.0f) / 2.0f - Math.Abs(f - (N - 1.0f) / 2.0f)));
            Console.WriteLine(melLogE);
        }

        // add to array
        melLogs[i] = melLogE;
        Console.WriteLine(melLogs[i]);
    }
    return melLogs;
}

                      
```
* https://social.msdn.microsoft.com/Forums/vstudio/ko-KR/55d42f3c-9998-4609-a8fc-714b068c7a58/compute-mfcc-in-c?forum=csharpgeneral



### Envelope Detection
* https://www.dsprelated.com/showarticle/938.php

