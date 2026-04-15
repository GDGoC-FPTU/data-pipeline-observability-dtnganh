# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-2A202600026
**Name:** Dang Tung Anh
**Date:** 15/4/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200. | 9 | Du lieu sach, chi con san pham hop le nen agent chon dung. |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 1 | Outlier gia rat lon lam agent chon sai san pham. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi dung Garbage Data, agent bi dan sai boi chat luong du lieu kem. File co duplicate ID lam mo ho nhan dang ban ghi, wrong data type nhu "ten dollars" lam he thong doc sai hoac bo qua ban ghi, null values lam thieu thong tin de loc. Quan trong nhat la outlier gia cuc lon (Nuclear Reactor 999999) trong cung category electronics. Logic agent chon san pham co gia cao nhat, nen outlier chiem uu the va dan den tra loi sai. Neu pipeline co validate/cleaning tot, cac ban ghi loi se bi loai bo, ket qua se gan voi thuc te hon.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Dong y. Prompt co the ro rang, nhung neu du lieu nen bi nhieu hoac sai, agent se ra quyet dinh sai. Du lieu sach giup mo hinh chon thong tin dung, ket qua on dinh va dang tin cay hon.
