# avalonia-code-live-template

1. Creates a simple Avalonia.DirectProperty
   ##### avadp
   ```
    /// <summary>
    /// Defines the <see cref="$Property$"/> property.
    /// </summary>
    public static readonly DirectProperty<$ClassName$, $Type$> $Property$Property =
        AvaloniaProperty.RegisterDirect<$ClassName$, $Type$>(
            nameof(ThenContent),
            o => o.$Property$,
            (o, v) => o.$Property$ = v,
            defaultBindingMode: BindingMode.TwoWay,
            enableDataValidation: true);

    // For direct properties we need to have a backing field
    private $Type$ _$Property_Private$;

    /// <summary>
    /// $PropertyComment$
    /// </summary>
    public $Type$ $Property$
    {
        get => _$Property_Private$;
        set => SetAndRaise(VIfProperty, ref _$Property_Private$, value);
    }
   ```

2. Creates a simple Avalonia.StyledProperty
    ##### avasp
    ```
        /// <summary>
        /// Defines the <see cref="$Property$"/> property.
        /// </summary>
        public static readonly StyledProperty<$Type$> $Property$Property =
            AvaloniaProperty.Register<$ClassName$, $Type$>(nameof($Property$));

        /// <summary>
        /// $PropertyComment$
        /// </summary>
        public $Type$ $Property$
        {
            get => GetValue($Property$Property);
            set => SetValue($Property$Property, value);
        }
    ```