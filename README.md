[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574082&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** email@example.com
**Name:** Dang Tung Anh

---

## Mo ta

Bai lab nay xay dung mot ETL pipeline (Extract - Transform - Load) don gian bang Python/Pandas de xu ly, chuan hoa du lieu (tu JSON sang CSV). Ben canh viec setup pipeline, bai lab con tien hanh Stress Test voi mot AI Agent de kiem tra su khac biet cua Agent khi dung Clean Data (du lieu sach) va Garbage Data (du lieu rac), tu do chung minh tam quan trong cua Data Quality trong Data Pipeline.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Tao file garbage_data.csv (du lieu co chu dich lam sai lech)
python generate_garbage.py

# Kiem tra ket qua Agent
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

- So luong records extract tu JSON: 5
- So luong records bi drop (Validation loi): 2 (do `price <= 0` va `category` rong)
- So luong records duoc luu lai vao CSV: 3 (duoc transform them cot `discounted_price`, chuan hoa `category` viet khoa chu cai dau, va luu vet `processed_at`)
- Agent Simulation Test: Agent dua ra quyet dinh hoan toan chinh xac khi dung `processed_data.csv`, the hien suc manh cua mot Data Pipeline vung chac va tam quan trong cua Quality Data. Nguoc lai, dung voi thong tin Outlier tren file `garbage_data.csv`, ket qua mang tinh hai huoc (nhan dang Nuclear Reactor).
