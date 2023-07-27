## Syntax Examples


### TypeScript
```
// JavaScript Coding Style is used here
// Just like with JavaScript, semicolons are most of the times not required

class VirtualPoint {

  // Typed, public/protected/private access modifiers
  // Optional modifier (?:)
  
  public x?: number;
  protected y: number;
  private z: number;
 
  // Constructors never have a return type
  constructor(x: number, y: number): {
    this.x = x;
    this.y = y;
  }
  
    protected doSomething(): {
        return
    }
}
```

### PHP

```
// PSR Coding Style is used here

namespace Folder\Subfolder; // current namespce (PSR-4 standard)
use OtherFolder\OtherSubfolder\ClassName // import from namespace

class VirtualPoint extends OtherClass implements SomeInterface
{
    // Typed, public/protected/private access modifiers
    // Optional modifier (?int)
    public ?int $x;
    protected int $y;
    private int $z;

    // Constructors never have a return type
    public __construct(int $x, int $y, int $z)
    {
        $this->x = $x;
        $this->y = $y;
        $this->z = $z;
    }
    
    // access modifier: protected
    // type modifiers: nullable/optional integer, integer
    // return type: null
    protected function doSomething(?int $x, int $y): null
    {
        return null;
    }

}
```

```
// Constructor property promotion
// Properties don't need to be declared, in order to be accessed internally

class CustomerDTO
{
    public function __construct(
        public string $name, 
        public string $email, 
        public DateTimeImmutable $birth_date,
    ) {}
}
```

### Python

```
# PEP 8 Coding Style is used here

from folderName.fileName import className # import module
import folderName.folderNameAsPackage.moduleName # Import module from package (folders with __init__.py files)

class VirtualPoint(OtherClass):
{
    # Typed, public/protected/private access modifiers
    x: int
    _y: int
    __z: int

    // Constructors never have a return type
    def __init__(self, int $x, int $y): {
        self.x = $x;
        self._y = $y;
        self.__z = $z;
    }
    
    // Access modifier, type hint, return type
    def _do_something(self, x: int, y: int) -> None:
    {
        pass
    }

}
```