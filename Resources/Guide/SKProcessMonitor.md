# 🗂 SKProcessMonitor

`SKProcessMonitor`는 `macOS` 운영체제 프로세스 (Process) 상태를 추적하여 Handling 할 수 있도록 기능을 제공합니다. 

프로세스 (Process) 상태를 추적할 수 있는 상태 값은 아래와 같습니다.

- exec: Process Exec'd

- exit: Process Exited

- fork: Process Forked

# Example Source

`SKProcessMonitor` 예제 소스코드는 아래와 같습니다.

```Swift
let monitor = SKProcessMonitor(pid: 3447, fflag: .exit) { decriptor, flag, rawValue in
    print("Receive Process Monitor: \(decriptor), \(flag), \(rawValue)")
}
        
OperationQueue.main.addOperation(monitor)

// Advises the operation object that it should stop executing its task.
monitor.cancel()
```

# License

`Universal SystemKit` is released under the MIT license. [See LICENSE](https://github.com/ChangYeop-Yang/Apple-SystemKit/blob/main/LICENSE) for details.

</br>

```TEXT
MIT License

Copyright (c) 2022 Universal-SystemKit

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
