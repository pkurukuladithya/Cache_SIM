# 🚀 Cache Simulator Web App
IE2064_ACOA (Advanced Computer Architecture) project — interactive cache simulator built with Python + Streamlit. Compare L1 vs L1+L2, replacement policies, and see hit/miss metrics and AMAT in real time.

## 👥 Team & Module
- Module: IE2064_ACOA (Advanced Computer Architecture)
- Student: PRAVEENA KURUKULADITHYA (SLIIT | IT23689862)
- Project Name: CacheWebSim

## 📝 Description
A web-based simulator to explore cache behavior. Configure cache size, block size, associativity, replacement policy, and access cycles; choose memory access patterns; visualize hit/miss behavior and estimated AMAT. Great for demonstrating how architectural knobs affect performance.

## ✨ Features
- Fully configurable cache parameters: size, block size, associativity, replacement policy, and access cycles.
- Optional L2 level to show multi-level cache benefits.
- Interactive sliders/dropdowns for quick experiments.
- Access patterns: Random or Sequential (extendable to more patterns).
- Live metrics:
  - L1 and L2 Hit Ratio
  - L1 and L2 Miss Ratio
  - Approximate AMAT
- Easy to extend for visual cache block simulation and advanced analytics.

## 📦 Requirements
- Python 3.8+
- Streamlit
- NumPy
- Matplotlib / Plotly (optional)

## ⚙️ Installation
1) Clone or download the project.  
2) Navigate to the project directory:  
   `cd CacheWebSim`  
3) (Optional) Create a virtual environment:  
   - Windows: `python -m venv venv && venv\Scripts\activate`  
   - Mac/Linux: `python -m venv venv && source venv/bin/activate`  
4) Install dependencies:  
   `pip install -r requirements.txt`

## ▶️ Running the App
1) Start Streamlit: `streamlit run app.py`  
2) A browser tab opens automatically.  
3) Use the sidebar to tune cache parameters and access patterns.  
4) Click “Run Simulation” to see:  
   - L1/L2 Hit Ratio  
   - L1/L2 Miss Ratio  
   - Average Memory Access Time (AMAT)

## 🗂️ File Structure
```
CacheWebSim/
├── app.py               # Streamlit UI
├── cache_simulator.py   # Cache simulation logic
├── requirements.txt     # Dependencies
└── README.md            # This guide
```

## 🔍 Simulation Details
- Cache Access: Check tag/index; on miss, access next level (L2 or main memory).
- Replacement Policies: LRU, FIFO, Random.
- Metrics:
  - Hit Ratio = Hits / Total Accesses
  - Miss Ratio = 1 – Hit Ratio
  - AMAT = L1 Access Time + (Miss Ratio × Miss Penalty)
- Extendable: Add more patterns (temporal locality, conflict-heavy traces) or visualize set contents.

## 🧭 Suggested Demos (for IE2064_ACOA)
- Replacement policy impact: LRU vs FIFO with same size/assoc.
- Conflict vs capacity: low-assoc vs higher-assoc caches under the same footprint.
- Multi-level benefit: L1-only vs L1+L2 with slower memory.
- Block size vs sequential access: small vs large blocks on sequential traces.

## 🚀 Future Improvements
- L3 cache visualization for multi-core scenarios.
- Real-time cache block display (color-coded hits/misses).
- Benchmark traces instead of only random/sequential.
- Hit ratio vs cache size/associativity graphs.
- Write policies (write-back vs write-through).

## 📄 License
For educational purposes and academic demonstrations. Feel free to modify and extend for personal or research use.
