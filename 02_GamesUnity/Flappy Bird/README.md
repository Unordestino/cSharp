### Faz o passaro ir pra clique do mouse
> Rigidbody2D: Controla a gravidade do game ``` private Rigidbody2D rig; ```
> 
> GetComponent: Acessa a gravidade do Rididbody2D ```   rig = GetComponent<Rigidbody2D>(); ```
>
> Input.GetMouseButtonDown(0): Condição usada no if para fazer o player voar com o click do mouse
```

   public float speed = 1f;
    private Rigidbody2D rig;

    // Start is called before the first frame update
    void Start()
    {
        rig = GetComponent<Rigidbody2D>();
        
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetMouseButtonDown(0))
        {
            rig.velocity = Vector2.up * speed;


        }
```
