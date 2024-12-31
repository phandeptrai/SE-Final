## Phụ thuộc quá mức vào TransactionParser:

* Lớp BankStatement sử dụng TransactionParser, nhưng TransactionParser lại thuộc sở hữu của StatementAnalyzer. Điều này dẫn đến việc không rõ lớp nào chịu trách nhiệm chính về việc phân tích cú pháp.
* Giải pháp: Di chuyển logic parseFile từ BankStatement vào StatementAnalyzer và tách riêng trách nhiệm.
## Phạm vi trách nhiệm chưa rõ ràng:

* Transaction có phương thức categorize() nhưng việc phân loại giao dịch lại phù hợp hơn để xử lý trong lớp StatementAnalyzer.
* Giải pháp: Xóa phương thức categorize() trong Transaction và đưa nó vào StatementAnalyzer.
## Quản lý danh sách parser chưa tối ưu:

* StatementAnalyzer chứa danh sách TransactionParser, nhưng không có cơ chế để đăng ký hoặc quản lý danh sách này. Điều này có thể dẫn đến rủi ro sử dụng parser không đúng loại.
* Giải pháp: Thêm phương thức đăng ký parser (registerParser) để quản lý danh sách.
