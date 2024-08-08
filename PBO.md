# PROJEK
```dart
void main() {
  // Daftar nilai siswa
  List<int> scores = [80, 90, 75, 88, 92];
  

  // Menambahkan nilai baru ke daftar
  addScore(scores, 85);
 

  // Menampilkan semua nilai siswa
  print("Daftar nilai siswa:");
  tampilkanSemuaNilai(scores);
  

  // Menghitung dan menampilkan nilai rata-rata
  double averageScore = calculateAverage(scores);
  print("\nNilai rata-rata siswa: $averageScore");
  

  // Menampilkan nilai di atas rata-rata
  print("\nNilai di atas rata-rata:");
  displayAboveAverageScores(scores, averageScore);
  

  // Memanggil demonstrateClosure untuk menampilkan contoh penggunaan closure
  demonstrateClosure();
}
  

// Function untuk menambahkan nilai ke daftar
void addScore(List<int> scores, int score) {
  scores.add(score);
}
  

// Function untuk menampilkan semua nilai
void tampilkanSemuaNilai(List<int> scores) {
  for (int i = 0; i < scores.length; i++) {
    print("Nilai ke-${i + 1}: ${scores[i]}");
  }
}
  

// Function untuk menghitung nilai rata-rata
double calculateAverage(List<int> scores) {
  int total = 0;
  for (int score in scores) {
    total += score;
  }
  return total / scores.length;
}
  

// Function untuk menampilkan nilai di atas rata-rata
void displayAboveAverageScores(List<int> scores, double average) {
  for (int score in scores) {
    if (score > average) {
      print(score);
    }
  }
}
  

// Scope dan closure
Function createMultiplier(int factor) {
  return (int value) {
    return value * factor;
  };
}
  

void demonstrateClosure() {
  var multiplyBy2 = createMultiplier(2);
  var multiplyBy3 = createMultiplier(3);
  

  print("\nContoh penggunaan closure:");
  print("2 * 2 = ${multiplyBy2(2)}");
  print("3 * 3 = ${multiplyBy3(3)}");
}
```