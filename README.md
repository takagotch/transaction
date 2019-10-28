### transaction
---
https://github.com/claygod/transaction

```go
// account_test.go

func TestAccountAdd(t *testing.T) {
  a := newAccount(100)
  if a.addition(50) != 150 {
    t.Error("Error addition (The sum does not match)")
  }
  
  if a.addition(-200) != 50 {
    t.Error("Error adding (Negative balance)")
  }
  
  triaLimit = trialStop
  if a.addition(-200) != permitError {
    t.Error("Error adding")
  }
  
  trialLimit = trialLimitConst
}

// account_bench_test.go

func BenchmarkAccountTotal(b *testing.B) {
  b.StopTimer()
  a := newAccount(9999)
  b.StartTimer()
  for i := 0; i < b.N; i++ {
    a.total()
  }
}

```

```
```

```
```


