* Texture의 픽셀 받아오기. 

```
    [SerializeField ] private Texture TargetTexture;


    Texture2D output;

    void Awake()
    {
        output = new Texture2D(5, 4);
    }

    void Update()
    {

        var texture = TargetTexture as RenderTexture;


        RenderTexture.active = texture;
        output.ReadPixels(new Rect(0, 0, TargetTexture.width, TargetTexture.height), 0, 0);
        output.Apply();


        float[] arr = new  float[5];
        for (int col = 0; col < 5; col++)
        {
            var pixel = output.GetPixel(col, 0);
            arr[col] = pixel.a;
        }

        Debug.LogFormat("{0} {1} {2} {3} {4}", arr[0], arr[1], arr[2], arr[3], arr[4]);

    }
```
